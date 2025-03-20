# Results vs. 3.13.0rc2

- fork: mpage
- ref: lfb_nolock
- machine: linux-x86_64
- commit hash: a350570
- commit date: 2025-03-19
- overall geometric mean: 1.037x slower
- HPT reliability: 99.42%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 288 ms: 1.11x slower                                        |
| docutils       | 2.63 sec                                                               | 2.75 sec: 1.05x slower                                      |
| html5lib       | 68.6 ms                                                                | 67.2 ms: 1.02x faster                                       |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 525 ms: 1.72x faster                                        |
| async_tree_io              | 881 ms                                                                 | 557 ms: 1.58x faster                                        |
| async_tree_none_tg         | 333 ms                                                                 | 225 ms: 1.48x faster                                        |
| async_tree_memoization     | 459 ms                                                                 | 322 ms: 1.43x faster                                        |
| async_tree_memoization_tg  | 410 ms                                                                 | 289 ms: 1.42x faster                                        |
| async_tree_none            | 353 ms                                                                 | 261 ms: 1.35x faster                                        |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 555 ms: 1.14x faster                                        |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 587 ms: 1.14x faster                                        |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                        |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                       |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 76.7 ms                                                                | 65.3 ms: 1.17x faster                                       |
| pidigits       | 216 ms                                                                 | 228 ms: 1.05x slower                                        |
| nbody          | 85.3 ms                                                                | 105 ms: 1.23x slower                                        |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.63 ms: 1.22x faster                                       |
| regex_dna      | 189 ms                                                                 | 165 ms: 1.14x faster                                        |
| regex_v8       | 23.2 ms                                                                | 21.0 ms: 1.11x faster                                       |
| regex_compile  | 131 ms                                                                 | 151 ms: 1.15x slower                                        |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.5 ms: 1.07x faster                                       |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                        |
| json_loads           | 27.3 us                                                                | 29.5 us: 1.08x slower                                       |
| tomli_loads          | 2.01 sec                                                               | 2.26 sec: 1.13x slower                                      |
| xml_etree_generate   | 85.4 ms                                                                | 96.3 ms: 1.13x slower                                       |
| unpickle_pure_python | 208 us                                                                 | 236 us: 1.14x slower                                        |
| xml_etree_process    | 59.2 ms                                                                | 68.7 ms: 1.16x slower                                       |
| pickle_pure_python   | 292 us                                                                 | 342 us: 1.17x slower                                        |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                       |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.7 ms: 1.43x slower                                       |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                       |
| Geometric mean         | (ref)                                                                  | 1.46x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 57.9 ms: 1.18x slower                                       |
| django_template | 34.2 ms                                                                | 41.4 ms: 1.21x slower                                       |
| genshi_text     | 21.7 ms                                                                | 26.9 ms: 1.24x slower                                       |
| mako            | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                       |
| Geometric mean  | (ref)                                                                  | 1.25x slower                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.79 ms: 1.85x faster                                       |
| async_tree_io_tg           | 901 ms                                                                 | 525 ms: 1.72x faster                                        |
| async_tree_io              | 881 ms                                                                 | 557 ms: 1.58x faster                                        |
| async_tree_none_tg         | 333 ms                                                                 | 225 ms: 1.48x faster                                        |
| async_tree_memoization     | 459 ms                                                                 | 322 ms: 1.43x faster                                        |
| async_tree_memoization_tg  | 410 ms                                                                 | 289 ms: 1.42x faster                                        |
| async_tree_none            | 353 ms                                                                 | 261 ms: 1.35x faster                                        |
| regex_effbot               | 3.21 ms                                                                | 2.63 ms: 1.22x faster                                       |
| deepcopy                   | 357 us                                                                 | 299 us: 1.20x faster                                        |
| float                      | 76.7 ms                                                                | 65.3 ms: 1.17x faster                                       |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 555 ms: 1.14x faster                                        |
| regex_dna                  | 189 ms                                                                 | 165 ms: 1.14x faster                                        |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 587 ms: 1.14x faster                                        |
| sqlite_synth               | 2.25 us                                                                | 2.02 us: 1.12x faster                                       |
| go                         | 141 ms                                                                 | 127 ms: 1.11x faster                                        |
| regex_v8                   | 23.2 ms                                                                | 21.0 ms: 1.11x faster                                       |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.5 ms: 1.07x faster                                       |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                        |
| scimark_sor                | 134 ms                                                                 | 127 ms: 1.05x faster                                        |
| deepcopy_memo              | 38.1 us                                                                | 36.5 us: 1.04x faster                                       |
| html5lib                   | 68.6 ms                                                                | 67.2 ms: 1.02x faster                                       |
| dulwich_log                | 74.5 ms                                                                | 73.1 ms: 1.02x faster                                       |
| deepcopy_reduce            | 3.12 us                                                                | 3.09 us: 1.01x faster                                       |
| spectral_norm              | 108 ms                                                                 | 107 ms: 1.01x faster                                        |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                        |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                       |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                      |
| create_gc_cycles           | 1.33 ms                                                                | 1.35 ms: 1.01x slower                                       |
| pathlib                    | 19.3 ms                                                                | 19.6 ms: 1.02x slower                                       |
| json                       | 4.98 ms                                                                | 5.06 ms: 1.02x slower                                       |
| pyflate                    | 449 ms                                                                 | 460 ms: 1.02x slower                                        |
| bpe_tokeniser              | 4.46 sec                                                               | 4.57 sec: 1.02x slower                                      |
| docutils                   | 2.63 sec                                                               | 2.75 sec: 1.05x slower                                      |
| pidigits                   | 216 ms                                                                 | 228 ms: 1.05x slower                                        |
| logging_silent             | 98.2 ns                                                                | 105 ns: 1.07x slower                                        |
| json_loads                 | 27.3 us                                                                | 29.5 us: 1.08x slower                                       |
| thrift                     | 772 us                                                                 | 837 us: 1.08x slower                                        |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.19 ms: 1.09x slower                                       |
| 2to3                       | 259 ms                                                                 | 288 ms: 1.11x slower                                        |
| pprint_safe_repr           | 719 ms                                                                 | 798 ms: 1.11x slower                                        |
| telco                      | 7.77 ms                                                                | 8.68 ms: 1.12x slower                                       |
| deltablue                  | 3.10 ms                                                                | 3.47 ms: 1.12x slower                                       |
| tomli_loads                | 2.01 sec                                                               | 2.26 sec: 1.13x slower                                      |
| scimark_monte_carlo        | 65.8 ms                                                                | 74.1 ms: 1.13x slower                                       |
| generators                 | 28.5 ms                                                                | 32.2 ms: 1.13x slower                                       |
| xml_etree_generate         | 85.4 ms                                                                | 96.3 ms: 1.13x slower                                       |
| chaos                      | 56.3 ms                                                                | 63.6 ms: 1.13x slower                                       |
| unpickle_pure_python       | 208 us                                                                 | 236 us: 1.14x slower                                        |
| pprint_pformat             | 1.46 sec                                                               | 1.65 sec: 1.14x slower                                      |
| logging_simple             | 6.14 us                                                                | 7.02 us: 1.14x slower                                       |
| regex_compile              | 131 ms                                                                 | 151 ms: 1.15x slower                                        |
| logging_format             | 6.92 us                                                                | 7.99 us: 1.16x slower                                       |
| xml_etree_process          | 59.2 ms                                                                | 68.7 ms: 1.16x slower                                       |
| coverage                   | 82.5 ms                                                                | 95.7 ms: 1.16x slower                                       |
| richards                   | 44.4 ms                                                                | 51.5 ms: 1.16x slower                                       |
| mdp                        | 2.34 sec                                                               | 2.73 sec: 1.16x slower                                      |
| raytrace                   | 250 ms                                                                 | 292 ms: 1.17x slower                                        |
| pickle_pure_python         | 292 us                                                                 | 342 us: 1.17x slower                                        |
| genshi_xml                 | 49.1 ms                                                                | 57.9 ms: 1.18x slower                                       |
| nqueens                    | 77.7 ms                                                                | 92.4 ms: 1.19x slower                                       |
| comprehensions             | 16.6 us                                                                | 19.8 us: 1.19x slower                                       |
| richards_super             | 50.4 ms                                                                | 60.2 ms: 1.20x slower                                       |
| sympy_integrate            | 19.7 ms                                                                | 23.6 ms: 1.20x slower                                       |
| sympy_sum                  | 154 ms                                                                 | 185 ms: 1.20x slower                                        |
| scimark_lu                 | 112 ms                                                                 | 135 ms: 1.20x slower                                        |
| fannkuch                   | 376 ms                                                                 | 452 ms: 1.20x slower                                        |
| sympy_expand               | 454 ms                                                                 | 546 ms: 1.20x slower                                        |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                       |
| django_template            | 34.2 ms                                                                | 41.4 ms: 1.21x slower                                       |
| sympy_str                  | 274 ms                                                                 | 332 ms: 1.21x slower                                        |
| hexiom                     | 5.95 ms                                                                | 7.27 ms: 1.22x slower                                       |
| crypto_pyaes               | 68.2 ms                                                                | 83.4 ms: 1.22x slower                                       |
| nbody                      | 85.3 ms                                                                | 105 ms: 1.23x slower                                        |
| genshi_text                | 21.7 ms                                                                | 26.9 ms: 1.24x slower                                       |
| meteor_contest             | 101 ms                                                                 | 126 ms: 1.24x slower                                        |
| typing_runtime_protocols   | 156 us                                                                 | 194 us: 1.25x slower                                        |
| mako                       | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                       |
| python_startup             | 11.0 ms                                                                | 15.7 ms: 1.43x slower                                       |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                       |
| bench_thread_pool          | 924 us                                                                 | 3.13 ms: 3.39x slower                                       |
| bench_mp_pool              | 11.0 ms                                                                | 96.7 ms: 8.79x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                |

Benchmark hidden because not significant (3): pylint, scimark_fft, asyncio_websockets
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250319-3.14.0a6+-a350570-NOGIL/bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.037x slower

# HPT report

- Reliability score: 99.42% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x