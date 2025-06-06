# Results vs. 3.13.0rc2

- fork: mpage
- ref: measure_latest_lfb
- machine: linux-x86_64
- commit hash: 80fc5aa
- commit date: 2025-03-23
- overall geometric mean: 1.057x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 250 ms: 1.04x faster                                                |
| docutils       | 2.63 sec                                                               | 2.57 sec: 1.02x faster                                              |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 312 ms: 1.47x faster                                                |
| async_tree_io_tg           | 901 ms                                                                 | 632 ms: 1.43x faster                                                |
| async_tree_io              | 881 ms                                                                 | 619 ms: 1.42x faster                                                |
| async_tree_memoization_tg  | 410 ms                                                                 | 303 ms: 1.35x faster                                                |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 505 ms: 1.32x faster                                                |
| async_tree_none_tg         | 333 ms                                                                 | 252 ms: 1.32x faster                                                |
| async_tree_none            | 353 ms                                                                 | 271 ms: 1.30x faster                                                |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 490 ms: 1.29x faster                                                |
| async_generators           | 375 ms                                                                 | 326 ms: 1.15x faster                                                |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                        |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 194 ms: 1.12x faster                                                |
| float          | 76.7 ms                                                                | 70.9 ms: 1.08x faster                                               |
| nbody          | 85.3 ms                                                                | 90.8 ms: 1.06x slower                                               |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.58 ms: 1.24x faster                                               |
| regex_dna      | 189 ms                                                                 | 173 ms: 1.09x faster                                                |
| regex_v8       | 23.2 ms                                                                | 21.8 ms: 1.06x faster                                               |
| regex_compile  | 131 ms                                                                 | 125 ms: 1.05x faster                                                |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.87 sec: 1.08x faster                                              |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.06x faster                                                |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.2 ms: 1.04x faster                                               |
| xml_etree_generate   | 85.4 ms                                                                | 83.0 ms: 1.03x faster                                               |
| xml_etree_process    | 59.2 ms                                                                | 58.4 ms: 1.01x faster                                               |
| json_loads           | 27.3 us                                                                | 27.2 us: 1.01x faster                                               |
| unpickle_pure_python | 208 us                                                                 | 213 us: 1.02x slower                                                |
| pickle_pure_python   | 292 us                                                                 | 302 us: 1.04x slower                                                |
| json_dumps           | 10.6 ms                                                                | 11.0 ms: 1.04x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.64 ms: 1.17x slower                                               |
| python_startup         | 11.0 ms                                                                | 15.0 ms: 1.36x slower                                               |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.5 ms: 1.06x faster                                               |
| genshi_xml      | 49.1 ms                                                                | 47.9 ms: 1.02x faster                                               |
| django_template | 34.2 ms                                                                | 34.5 ms: 1.01x slower                                               |
| mako            | 11.2 ms                                                                | 11.9 ms: 1.06x slower                                               |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 312 ms: 1.47x faster                                                |
| async_tree_io_tg           | 901 ms                                                                 | 632 ms: 1.43x faster                                                |
| async_tree_io              | 881 ms                                                                 | 619 ms: 1.42x faster                                                |
| deepcopy                   | 357 us                                                                 | 252 us: 1.42x faster                                                |
| async_tree_memoization_tg  | 410 ms                                                                 | 303 ms: 1.35x faster                                                |
| deepcopy_memo              | 38.1 us                                                                | 28.6 us: 1.33x faster                                               |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 505 ms: 1.32x faster                                                |
| async_tree_none_tg         | 333 ms                                                                 | 252 ms: 1.32x faster                                                |
| async_tree_none            | 353 ms                                                                 | 271 ms: 1.30x faster                                                |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 490 ms: 1.29x faster                                                |
| go                         | 141 ms                                                                 | 109 ms: 1.29x faster                                                |
| regex_effbot               | 3.21 ms                                                                | 2.58 ms: 1.24x faster                                               |
| scimark_sor                | 134 ms                                                                 | 111 ms: 1.20x faster                                                |
| deepcopy_reduce            | 3.12 us                                                                | 2.64 us: 1.18x faster                                               |
| spectral_norm              | 108 ms                                                                 | 92.9 ms: 1.16x faster                                               |
| async_generators           | 375 ms                                                                 | 326 ms: 1.15x faster                                                |
| pylint                     | 317 ms                                                                 | 282 ms: 1.13x faster                                                |
| pidigits                   | 216 ms                                                                 | 194 ms: 1.12x faster                                                |
| dulwich_log                | 74.5 ms                                                                | 67.4 ms: 1.11x faster                                               |
| pyflate                    | 449 ms                                                                 | 408 ms: 1.10x faster                                                |
| scimark_fft                | 348 ms                                                                 | 318 ms: 1.09x faster                                                |
| regex_dna                  | 189 ms                                                                 | 173 ms: 1.09x faster                                                |
| float                      | 76.7 ms                                                                | 70.9 ms: 1.08x faster                                               |
| tomli_loads                | 2.01 sec                                                               | 1.87 sec: 1.08x faster                                              |
| richards                   | 44.4 ms                                                                | 41.3 ms: 1.08x faster                                               |
| richards_super             | 50.4 ms                                                                | 47.2 ms: 1.07x faster                                               |
| regex_v8                   | 23.2 ms                                                                | 21.8 ms: 1.06x faster                                               |
| genshi_text                | 21.7 ms                                                                | 20.5 ms: 1.06x faster                                               |
| telco                      | 7.77 ms                                                                | 7.35 ms: 1.06x faster                                               |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.06x faster                                                |
| regex_compile              | 131 ms                                                                 | 125 ms: 1.05x faster                                                |
| generators                 | 28.5 ms                                                                | 27.1 ms: 1.05x faster                                               |
| logging_silent             | 98.2 ns                                                                | 93.9 ns: 1.05x faster                                               |
| 2to3                       | 259 ms                                                                 | 250 ms: 1.04x faster                                                |
| bpe_tokeniser              | 4.46 sec                                                               | 4.29 sec: 1.04x faster                                              |
| scimark_monte_carlo        | 65.8 ms                                                                | 63.5 ms: 1.04x faster                                               |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.2 ms: 1.04x faster                                               |
| pprint_safe_repr           | 719 ms                                                                 | 697 ms: 1.03x faster                                                |
| json                       | 4.98 ms                                                                | 4.84 ms: 1.03x faster                                               |
| xml_etree_generate         | 85.4 ms                                                                | 83.0 ms: 1.03x faster                                               |
| pprint_pformat             | 1.46 sec                                                               | 1.42 sec: 1.03x faster                                              |
| coverage                   | 82.5 ms                                                                | 80.4 ms: 1.03x faster                                               |
| genshi_xml                 | 49.1 ms                                                                | 47.9 ms: 1.02x faster                                               |
| mdp                        | 2.34 sec                                                               | 2.29 sec: 1.02x faster                                              |
| meteor_contest             | 101 ms                                                                 | 99.1 ms: 1.02x faster                                               |
| docutils                   | 2.63 sec                                                               | 2.57 sec: 1.02x faster                                              |
| chaos                      | 56.3 ms                                                                | 55.2 ms: 1.02x faster                                               |
| pycparser                  | 1.12 sec                                                               | 1.10 sec: 1.02x faster                                              |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.68 ms: 1.01x faster                                               |
| xml_etree_process          | 59.2 ms                                                                | 58.4 ms: 1.01x faster                                               |
| sympy_integrate            | 19.7 ms                                                                | 19.5 ms: 1.01x faster                                               |
| logging_format             | 6.92 us                                                                | 6.84 us: 1.01x faster                                               |
| sympy_str                  | 274 ms                                                                 | 272 ms: 1.01x faster                                                |
| pathlib                    | 19.3 ms                                                                | 19.1 ms: 1.01x faster                                               |
| json_loads                 | 27.3 us                                                                | 27.2 us: 1.01x faster                                               |
| raytrace                   | 250 ms                                                                 | 249 ms: 1.00x faster                                                |
| sympy_sum                  | 154 ms                                                                 | 155 ms: 1.01x slower                                                |
| django_template            | 34.2 ms                                                                | 34.5 ms: 1.01x slower                                               |
| sympy_expand               | 454 ms                                                                 | 458 ms: 1.01x slower                                                |
| nqueens                    | 77.7 ms                                                                | 78.5 ms: 1.01x slower                                               |
| scimark_lu                 | 112 ms                                                                 | 114 ms: 1.01x slower                                                |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                               |
| crypto_pyaes               | 68.2 ms                                                                | 69.8 ms: 1.02x slower                                               |
| unpickle_pure_python       | 208 us                                                                 | 213 us: 1.02x slower                                                |
| pickle_pure_python         | 292 us                                                                 | 302 us: 1.04x slower                                                |
| fannkuch                   | 376 ms                                                                 | 390 ms: 1.04x slower                                                |
| json_dumps                 | 10.6 ms                                                                | 11.0 ms: 1.04x slower                                               |
| deltablue                  | 3.10 ms                                                                | 3.24 ms: 1.05x slower                                               |
| mako                       | 11.2 ms                                                                | 11.9 ms: 1.06x slower                                               |
| nbody                      | 85.3 ms                                                                | 90.8 ms: 1.06x slower                                               |
| bench_thread_pool          | 924 us                                                                 | 1.04 ms: 1.13x slower                                               |
| python_startup_no_site     | 7.41 ms                                                                | 8.64 ms: 1.17x slower                                               |
| gc_traversal               | 3.32 ms                                                                | 4.08 ms: 1.23x slower                                               |
| python_startup             | 11.0 ms                                                                | 15.0 ms: 1.36x slower                                               |
| create_gc_cycles           | 1.33 ms                                                                | 1.86 ms: 1.40x slower                                               |
| bench_mp_pool              | 11.0 ms                                                                | 90.0 ms: 8.18x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                        |

Benchmark hidden because not significant (7): thrift, sqlite_synth, comprehensions, typing_runtime_protocols, logging_simple, asyncio_websockets, hexiom
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250323-3.14.0a6+-80fc5aa/bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.057x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.12x