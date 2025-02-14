# Results vs. default_base_vs_NOGIL

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 68b535b
- commit date: 2025-02-13
- overall geometric mean: 1.107x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 298 ms: 1.16x slower                                              |
| docutils       | 2.57 sec                                                               | 2.75 sec: 1.07x slower                                            |
| sphinx         | 981 ms                                                                 | 1.09 sec: 1.11x slower                                            |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg          | 628 ms                                                                 | 572 ms: 1.10x faster                                              |
| async_tree_io             | 622 ms                                                                 | 599 ms: 1.04x faster                                              |
| async_tree_none_tg        | 265 ms                                                                 | 256 ms: 1.04x faster                                              |
| async_tree_memoization_tg | 320 ms                                                                 | 314 ms: 1.02x faster                                              |
| coroutines                | 22.2 ms                                                                | 22.1 ms: 1.01x faster                                             |
| async_tree_cpu_io_mixed   | 514 ms                                                                 | 535 ms: 1.04x slower                                              |
| async_tree_none           | 269 ms                                                                 | 282 ms: 1.05x slower                                              |
| async_tree_memoization    | 326 ms                                                                 | 346 ms: 1.06x slower                                              |
| async_generators          | 326 ms                                                                 | 368 ms: 1.13x slower                                              |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 72.5 ms                                                                | 76.1 ms: 1.05x slower                                             |
| pidigits       | 184 ms                                                                 | 212 ms: 1.15x slower                                              |
| nbody          | 91.6 ms                                                                | 129 ms: 1.41x slower                                              |
| Geometric mean | (ref)                                                                  | 1.20x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 2.84 ms                                                                | 2.79 ms: 1.02x faster                                             |
| regex_v8       | 24.3 ms                                                                | 24.3 ms: 1.00x faster                                             |
| regex_dna      | 168 ms                                                                 | 180 ms: 1.07x slower                                              |
| regex_compile  | 128 ms                                                                 | 145 ms: 1.14x slower                                              |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 91.5 ms                                                                | 87.4 ms: 1.05x faster                                             |
| unpickle_pure_python | 220 us                                                                 | 239 us: 1.09x slower                                              |
| json_loads           | 28.9 us                                                                | 31.6 us: 1.09x slower                                             |
| pickle_pure_python   | 318 us                                                                 | 348 us: 1.09x slower                                              |
| json_dumps           | 11.4 ms                                                                | 12.7 ms: 1.11x slower                                             |
| xml_etree_generate   | 83.4 ms                                                                | 94.5 ms: 1.13x slower                                             |
| xml_etree_process    | 58.9 ms                                                                | 68.6 ms: 1.17x slower                                             |
| tomli_loads          | 1.95 sec                                                               | 2.27 sec: 1.17x slower                                            |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                      |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.4 ms: 1.05x slower                                             |
| python_startup_no_site | 7.48 ms                                                                | 9.70 ms: 1.30x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 34.6 ms                                                                | 41.4 ms: 1.20x slower                                             |
| genshi_xml      | 48.6 ms                                                                | 58.6 ms: 1.21x slower                                             |
| genshi_text     | 21.6 ms                                                                | 26.7 ms: 1.23x slower                                             |
| mako            | 11.7 ms                                                                | 15.6 ms: 1.33x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.24x slower                                                      |

All benchmarks:
===============

| Benchmark                 | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal              | 4.43 ms                                                                | 1.73 ms: 2.56x faster                                             |
| create_gc_cycles          | 1.86 ms                                                                | 1.37 ms: 1.35x faster                                             |
| async_tree_io_tg          | 628 ms                                                                 | 572 ms: 1.10x faster                                              |
| sqlite_synth              | 2.20 us                                                                | 2.06 us: 1.07x faster                                             |
| xml_etree_iterparse       | 91.5 ms                                                                | 87.4 ms: 1.05x faster                                             |
| async_tree_io             | 622 ms                                                                 | 599 ms: 1.04x faster                                              |
| async_tree_none_tg        | 265 ms                                                                 | 256 ms: 1.04x faster                                              |
| async_tree_memoization_tg | 320 ms                                                                 | 314 ms: 1.02x faster                                              |
| regex_effbot              | 2.84 ms                                                                | 2.79 ms: 1.02x faster                                             |
| coroutines                | 22.2 ms                                                                | 22.1 ms: 1.01x faster                                             |
| regex_v8                  | 24.3 ms                                                                | 24.3 ms: 1.00x faster                                             |
| generators                | 29.9 ms                                                                | 30.2 ms: 1.01x slower                                             |
| pathlib                   | 18.7 ms                                                                | 19.1 ms: 1.02x slower                                             |
| pycparser                 | 1.13 sec                                                               | 1.17 sec: 1.03x slower                                            |
| async_tree_cpu_io_mixed   | 514 ms                                                                 | 535 ms: 1.04x slower                                              |
| async_tree_none           | 269 ms                                                                 | 282 ms: 1.05x slower                                              |
| scimark_sor               | 119 ms                                                                 | 125 ms: 1.05x slower                                              |
| float                     | 72.5 ms                                                                | 76.1 ms: 1.05x slower                                             |
| python_startup            | 14.7 ms                                                                | 15.4 ms: 1.05x slower                                             |
| json                      | 5.15 ms                                                                | 5.43 ms: 1.05x slower                                             |
| async_tree_memoization    | 326 ms                                                                 | 346 ms: 1.06x slower                                              |
| docutils                  | 2.57 sec                                                               | 2.75 sec: 1.07x slower                                            |
| regex_dna                 | 168 ms                                                                 | 180 ms: 1.07x slower                                              |
| dulwich_log               | 75.8 ms                                                                | 81.6 ms: 1.08x slower                                             |
| logging_silent            | 105 ns                                                                 | 113 ns: 1.08x slower                                              |
| bench_mp_pool             | 87.7 ms                                                                | 95.0 ms: 1.08x slower                                             |
| unpickle_pure_python      | 220 us                                                                 | 239 us: 1.09x slower                                              |
| json_loads                | 28.9 us                                                                | 31.6 us: 1.09x slower                                             |
| bpe_tokeniser             | 4.22 sec                                                               | 4.62 sec: 1.09x slower                                            |
| pickle_pure_python        | 318 us                                                                 | 348 us: 1.09x slower                                              |
| json_dumps                | 11.4 ms                                                                | 12.7 ms: 1.11x slower                                             |
| sphinx                    | 981 ms                                                                 | 1.09 sec: 1.11x slower                                            |
| spectral_norm             | 91.6 ms                                                                | 102 ms: 1.11x slower                                              |
| go                        | 119 ms                                                                 | 134 ms: 1.12x slower                                              |
| pylint                    | 279 ms                                                                 | 314 ms: 1.12x slower                                              |
| k_core                    | 2.04 sec                                                               | 2.29 sec: 1.12x slower                                            |
| async_generators          | 326 ms                                                                 | 368 ms: 1.13x slower                                              |
| xml_etree_generate        | 83.4 ms                                                                | 94.5 ms: 1.13x slower                                             |
| regex_compile             | 128 ms                                                                 | 145 ms: 1.14x slower                                              |
| many_optionals            | 1.01 ms                                                                | 1.16 ms: 1.14x slower                                             |
| sqlglot_normalize         | 102 ms                                                                 | 117 ms: 1.14x slower                                              |
| subparsers                | 21.8 ms                                                                | 25.0 ms: 1.15x slower                                             |
| pidigits                  | 184 ms                                                                 | 212 ms: 1.15x slower                                              |
| telco                     | 7.30 ms                                                                | 8.44 ms: 1.16x slower                                             |
| pprint_safe_repr          | 701 ms                                                                 | 815 ms: 1.16x slower                                              |
| 2to3                      | 256 ms                                                                 | 298 ms: 1.16x slower                                              |
| logging_simple            | 5.89 us                                                                | 6.87 us: 1.17x slower                                             |
| sqlglot_optimize          | 51.4 ms                                                                | 59.9 ms: 1.17x slower                                             |
| xml_etree_process         | 58.9 ms                                                                | 68.6 ms: 1.17x slower                                             |
| pprint_pformat            | 1.43 sec                                                               | 1.68 sec: 1.17x slower                                            |
| tomli_loads               | 1.95 sec                                                               | 2.27 sec: 1.17x slower                                            |
| pyflate                   | 423 ms                                                                 | 495 ms: 1.17x slower                                              |
| mdp                       | 2.33 sec                                                               | 2.73 sec: 1.17x slower                                            |
| hexiom                    | 6.01 ms                                                                | 7.08 ms: 1.18x slower                                             |
| deltablue                 | 3.22 ms                                                                | 3.80 ms: 1.18x slower                                             |
| nqueens                   | 79.5 ms                                                                | 94.0 ms: 1.18x slower                                             |
| sqlglot_transpile         | 1.59 ms                                                                | 1.89 ms: 1.18x slower                                             |
| scimark_lu                | 114 ms                                                                 | 135 ms: 1.19x slower                                              |
| logging_format            | 6.61 us                                                                | 7.85 us: 1.19x slower                                             |
| comprehensions            | 16.4 us                                                                | 19.5 us: 1.19x slower                                             |
| chaos                     | 56.5 ms                                                                | 67.6 ms: 1.20x slower                                             |
| django_template           | 34.6 ms                                                                | 41.4 ms: 1.20x slower                                             |
| raytrace                  | 265 ms                                                                 | 318 ms: 1.20x slower                                              |
| sympy_expand              | 450 ms                                                                 | 540 ms: 1.20x slower                                              |
| sympy_sum                 | 152 ms                                                                 | 183 ms: 1.20x slower                                              |
| genshi_xml                | 48.6 ms                                                                | 58.6 ms: 1.21x slower                                             |
| scimark_fft               | 314 ms                                                                 | 380 ms: 1.21x slower                                              |
| sympy_integrate           | 19.7 ms                                                                | 23.8 ms: 1.21x slower                                             |
| sqlalchemy_declarative    | 127 ms                                                                 | 155 ms: 1.21x slower                                              |
| deepcopy                  | 252 us                                                                 | 305 us: 1.21x slower                                              |
| deepcopy_reduce           | 2.61 us                                                                | 3.17 us: 1.22x slower                                             |
| thrift                    | 735 us                                                                 | 896 us: 1.22x slower                                              |
| coverage                  | 80.1 ms                                                                | 97.6 ms: 1.22x slower                                             |
| sqlglot_parse             | 1.29 ms                                                                | 1.58 ms: 1.22x slower                                             |
| sympy_str                 | 269 ms                                                                 | 330 ms: 1.23x slower                                              |
| genshi_text               | 21.6 ms                                                                | 26.7 ms: 1.23x slower                                             |
| shortest_path             | 431 ms                                                                 | 538 ms: 1.25x slower                                              |
| richards                  | 43.8 ms                                                                | 54.7 ms: 1.25x slower                                             |
| connected_components      | 388 ms                                                                 | 486 ms: 1.25x slower                                              |
| sqlalchemy_imperative     | 19.2 ms                                                                | 24.0 ms: 1.25x slower                                             |
| fannkuch                  | 380 ms                                                                 | 477 ms: 1.26x slower                                              |
| scimark_monte_carlo       | 65.1 ms                                                                | 82.1 ms: 1.26x slower                                             |
| deepcopy_memo             | 30.3 us                                                                | 38.3 us: 1.26x slower                                             |
| scimark_sparse_mat_mult   | 4.40 ms                                                                | 5.58 ms: 1.27x slower                                             |
| crypto_pyaes              | 68.7 ms                                                                | 87.4 ms: 1.27x slower                                             |
| meteor_contest            | 99.4 ms                                                                | 127 ms: 1.28x slower                                              |
| typing_runtime_protocols  | 155 us                                                                 | 198 us: 1.28x slower                                              |
| richards_super            | 49.3 ms                                                                | 63.3 ms: 1.28x slower                                             |
| python_startup_no_site    | 7.48 ms                                                                | 9.70 ms: 1.30x slower                                             |
| mako                      | 11.7 ms                                                                | 15.6 ms: 1.33x slower                                             |
| nbody                     | 91.6 ms                                                                | 129 ms: 1.41x slower                                              |
| bench_thread_pool         | 1.03 ms                                                                | 3.32 ms: 3.24x slower                                             |
| Geometric mean            | (ref)                                                                  | 1.13x slower                                                      |

Benchmark hidden because not significant (3): asyncio_websockets, xml_etree_parse, async_tree_cpu_io_mixed_tg
Ignored benchmarks (1) of results/bm-20250213-3.14.0a5+-68b535b-NOGIL/bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b.json: html5lib

- Geometric mean (including insignificant results): 1.107x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.21x