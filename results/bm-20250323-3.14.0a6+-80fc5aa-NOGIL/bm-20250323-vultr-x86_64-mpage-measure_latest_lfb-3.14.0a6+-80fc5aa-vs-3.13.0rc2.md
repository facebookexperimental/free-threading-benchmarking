# Results vs. 3.13.0rc2

- fork: mpage
- ref: measure_latest_lfb
- machine: linux-x86_64
- commit hash: 80fc5aa
- commit date: 2025-03-23
- overall geometric mean: 1.054x slower
- HPT reliability: 99.87%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 289 ms: 1.12x slower                                                |
| docutils       | 2.63 sec                                                               | 2.75 sec: 1.05x slower                                              |
| html5lib       | 68.6 ms                                                                | 68.1 ms: 1.01x faster                                               |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 541 ms: 1.66x faster                                                |
| async_tree_io              | 881 ms                                                                 | 573 ms: 1.54x faster                                                |
| async_tree_none_tg         | 333 ms                                                                 | 233 ms: 1.43x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 326 ms: 1.41x faster                                                |
| async_tree_memoization_tg  | 410 ms                                                                 | 294 ms: 1.40x faster                                                |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 478 ms: 1.33x faster                                                |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 512 ms: 1.30x faster                                                |
| async_tree_none            | 353 ms                                                                 | 274 ms: 1.29x faster                                                |
| async_generators           | 375 ms                                                                 | 380 ms: 1.01x slower                                                |
| coroutines                 | 23.3 ms                                                                | 23.7 ms: 1.01x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.28x faster                                                        |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 198 ms: 1.09x faster                                                |
| float          | 76.7 ms                                                                | 71.8 ms: 1.07x faster                                               |
| nbody          | 85.3 ms                                                                | 120 ms: 1.41x slower                                                |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.73 ms: 1.18x faster                                               |
| regex_dna      | 189 ms                                                                 | 168 ms: 1.12x faster                                                |
| regex_v8       | 23.2 ms                                                                | 21.3 ms: 1.09x faster                                               |
| regex_compile  | 131 ms                                                                 | 153 ms: 1.17x slower                                                |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.6 ms: 1.08x faster                                               |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                |
| json_loads           | 27.3 us                                                                | 29.8 us: 1.09x slower                                               |
| tomli_loads          | 2.01 sec                                                               | 2.25 sec: 1.12x slower                                              |
| xml_etree_generate   | 85.4 ms                                                                | 96.7 ms: 1.13x slower                                               |
| unpickle_pure_python | 208 us                                                                 | 244 us: 1.17x slower                                                |
| pickle_pure_python   | 292 us                                                                 | 343 us: 1.18x slower                                                |
| xml_etree_process    | 59.2 ms                                                                | 70.7 ms: 1.19x slower                                               |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                               |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                               |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 57.8 ms: 1.18x slower                                               |
| django_template | 34.2 ms                                                                | 41.8 ms: 1.22x slower                                               |
| genshi_text     | 21.7 ms                                                                | 27.1 ms: 1.25x slower                                               |
| mako            | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                               |
| Geometric mean  | (ref)                                                                  | 1.26x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.79 ms: 1.86x faster                                               |
| async_tree_io_tg           | 901 ms                                                                 | 541 ms: 1.66x faster                                                |
| async_tree_io              | 881 ms                                                                 | 573 ms: 1.54x faster                                                |
| async_tree_none_tg         | 333 ms                                                                 | 233 ms: 1.43x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 326 ms: 1.41x faster                                                |
| async_tree_memoization_tg  | 410 ms                                                                 | 294 ms: 1.40x faster                                                |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 478 ms: 1.33x faster                                                |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 512 ms: 1.30x faster                                                |
| async_tree_none            | 353 ms                                                                 | 274 ms: 1.29x faster                                                |
| deepcopy                   | 357 us                                                                 | 301 us: 1.19x faster                                                |
| regex_effbot               | 3.21 ms                                                                | 2.73 ms: 1.18x faster                                               |
| sqlite_synth               | 2.25 us                                                                | 2.00 us: 1.12x faster                                               |
| regex_dna                  | 189 ms                                                                 | 168 ms: 1.12x faster                                                |
| pidigits                   | 216 ms                                                                 | 198 ms: 1.09x faster                                                |
| regex_v8                   | 23.2 ms                                                                | 21.3 ms: 1.09x faster                                               |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.6 ms: 1.08x faster                                               |
| float                      | 76.7 ms                                                                | 71.8 ms: 1.07x faster                                               |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                |
| go                         | 141 ms                                                                 | 135 ms: 1.04x faster                                                |
| scimark_sor                | 134 ms                                                                 | 129 ms: 1.03x faster                                                |
| deepcopy_memo              | 38.1 us                                                                | 37.3 us: 1.02x faster                                               |
| html5lib                   | 68.6 ms                                                                | 68.1 ms: 1.01x faster                                               |
| deepcopy_reduce            | 3.12 us                                                                | 3.10 us: 1.01x faster                                               |
| create_gc_cycles           | 1.33 ms                                                                | 1.34 ms: 1.01x slower                                               |
| json                       | 4.98 ms                                                                | 5.04 ms: 1.01x slower                                               |
| async_generators           | 375 ms                                                                 | 380 ms: 1.01x slower                                                |
| coroutines                 | 23.3 ms                                                                | 23.7 ms: 1.01x slower                                               |
| spectral_norm              | 108 ms                                                                 | 109 ms: 1.02x slower                                                |
| pathlib                    | 19.3 ms                                                                | 19.8 ms: 1.03x slower                                               |
| docutils                   | 2.63 sec                                                               | 2.75 sec: 1.05x slower                                              |
| scimark_fft                | 348 ms                                                                 | 364 ms: 1.05x slower                                                |
| pycparser                  | 1.12 sec                                                               | 1.18 sec: 1.05x slower                                              |
| bpe_tokeniser              | 4.46 sec                                                               | 4.72 sec: 1.06x slower                                              |
| pyflate                    | 449 ms                                                                 | 489 ms: 1.09x slower                                                |
| json_loads                 | 27.3 us                                                                | 29.8 us: 1.09x slower                                               |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.21 ms: 1.10x slower                                               |
| 2to3                       | 259 ms                                                                 | 289 ms: 1.12x slower                                                |
| tomli_loads                | 2.01 sec                                                               | 2.25 sec: 1.12x slower                                              |
| logging_silent             | 98.2 ns                                                                | 111 ns: 1.13x slower                                                |
| thrift                     | 772 us                                                                 | 872 us: 1.13x slower                                                |
| xml_etree_generate         | 85.4 ms                                                                | 96.7 ms: 1.13x slower                                               |
| pprint_safe_repr           | 719 ms                                                                 | 816 ms: 1.14x slower                                                |
| telco                      | 7.77 ms                                                                | 8.94 ms: 1.15x slower                                               |
| pprint_pformat             | 1.46 sec                                                               | 1.68 sec: 1.16x slower                                              |
| regex_compile              | 131 ms                                                                 | 153 ms: 1.17x slower                                                |
| mdp                        | 2.34 sec                                                               | 2.74 sec: 1.17x slower                                              |
| unpickle_pure_python       | 208 us                                                                 | 244 us: 1.17x slower                                                |
| pickle_pure_python         | 292 us                                                                 | 343 us: 1.18x slower                                                |
| genshi_xml                 | 49.1 ms                                                                | 57.8 ms: 1.18x slower                                               |
| chaos                      | 56.3 ms                                                                | 66.4 ms: 1.18x slower                                               |
| logging_format             | 6.92 us                                                                | 8.16 us: 1.18x slower                                               |
| generators                 | 28.5 ms                                                                | 33.7 ms: 1.18x slower                                               |
| sympy_integrate            | 19.7 ms                                                                | 23.4 ms: 1.19x slower                                               |
| logging_simple             | 6.14 us                                                                | 7.32 us: 1.19x slower                                               |
| xml_etree_process          | 59.2 ms                                                                | 70.7 ms: 1.19x slower                                               |
| deltablue                  | 3.10 ms                                                                | 3.70 ms: 1.20x slower                                               |
| scimark_monte_carlo        | 65.8 ms                                                                | 78.9 ms: 1.20x slower                                               |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                               |
| richards                   | 44.4 ms                                                                | 53.8 ms: 1.21x slower                                               |
| sympy_sum                  | 154 ms                                                                 | 187 ms: 1.21x slower                                                |
| sympy_str                  | 274 ms                                                                 | 332 ms: 1.21x slower                                                |
| django_template            | 34.2 ms                                                                | 41.8 ms: 1.22x slower                                               |
| raytrace                   | 250 ms                                                                 | 307 ms: 1.23x slower                                                |
| comprehensions             | 16.6 us                                                                | 20.4 us: 1.23x slower                                               |
| scimark_lu                 | 112 ms                                                                 | 138 ms: 1.23x slower                                                |
| sympy_expand               | 454 ms                                                                 | 558 ms: 1.23x slower                                                |
| richards_super             | 50.4 ms                                                                | 62.1 ms: 1.23x slower                                               |
| fannkuch                   | 376 ms                                                                 | 466 ms: 1.24x slower                                                |
| nqueens                    | 77.7 ms                                                                | 96.6 ms: 1.24x slower                                               |
| typing_runtime_protocols   | 156 us                                                                 | 194 us: 1.24x slower                                                |
| hexiom                     | 5.95 ms                                                                | 7.42 ms: 1.25x slower                                               |
| genshi_text                | 21.7 ms                                                                | 27.1 ms: 1.25x slower                                               |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.26x slower                                                |
| crypto_pyaes               | 68.2 ms                                                                | 85.9 ms: 1.26x slower                                               |
| coverage                   | 82.5 ms                                                                | 107 ms: 1.30x slower                                                |
| mako                       | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                               |
| nbody                      | 85.3 ms                                                                | 120 ms: 1.41x slower                                                |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                               |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                               |
| bench_thread_pool          | 924 us                                                                 | 3.14 ms: 3.40x slower                                               |
| bench_mp_pool              | 11.0 ms                                                                | 97.1 ms: 8.83x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                        |

Benchmark hidden because not significant (3): pylint, dulwich_log, asyncio_websockets
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250323-3.14.0a6+-80fc5aa-NOGIL/bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.054x slower

# HPT report

- Reliability score: 99.87% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.36x