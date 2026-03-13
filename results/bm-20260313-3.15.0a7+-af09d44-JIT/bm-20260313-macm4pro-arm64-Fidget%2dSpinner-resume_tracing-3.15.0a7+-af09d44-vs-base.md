# Results vs. base

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: af09d44
- commit date: 2026-03-13
- overall geometric mean: 1.037x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7+-0adc728 | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 119 ms                                                                   | 111 ms: 1.07x faster                                                         |
| docutils       | 1.01 sec                                                                 | 963 ms: 1.05x faster                                                         |
| html5lib       | 20.4 ms                                                                  | 19.2 ms: 1.06x faster                                                        |
| sphinx         | 400 ms                                                                   | 388 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7+-0adc728 | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| coroutines                       | 10.9 ms                                                                  | 9.15 ms: 1.19x faster                                                        |
| async_tree_io                    | 232 ms                                                                   | 207 ms: 1.12x faster                                                         |
| async_tree_none_tg               | 99.0 ms                                                                  | 90.9 ms: 1.09x faster                                                        |
| async_tree_none                  | 97.2 ms                                                                  | 89.5 ms: 1.09x faster                                                        |
| async_tree_eager_io              | 223 ms                                                                   | 205 ms: 1.09x faster                                                         |
| async_tree_io_tg                 | 226 ms                                                                   | 208 ms: 1.08x faster                                                         |
| async_tree_eager_io_tg           | 220 ms                                                                   | 203 ms: 1.08x faster                                                         |
| async_generators                 | 191 ms                                                                   | 178 ms: 1.08x faster                                                         |
| async_tree_eager_tg              | 82.5 ms                                                                  | 77.2 ms: 1.07x faster                                                        |
| async_tree_memoization_tg        | 136 ms                                                                   | 129 ms: 1.06x faster                                                         |
| async_tree_memoization           | 134 ms                                                                   | 127 ms: 1.06x faster                                                         |
| async_tree_eager_memoization_tg  | 121 ms                                                                   | 116 ms: 1.05x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 250 ms                                                                   | 241 ms: 1.04x faster                                                         |
| async_tree_cpu_io_mixed          | 249 ms                                                                   | 240 ms: 1.04x faster                                                         |
| async_tree_eager                 | 37.5 ms                                                                  | 36.3 ms: 1.03x faster                                                        |
| async_tree_eager_memoization     | 104 ms                                                                   | 101 ms: 1.03x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 241 ms                                                                   | 235 ms: 1.03x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 218 ms                                                                   | 212 ms: 1.02x faster                                                         |
| asyncio_websockets               | 188 ms                                                                   | 185 ms: 1.02x faster                                                         |
| Geometric mean                   | (ref)                                                                    | 1.07x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7+-0adc728 | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 165 ms                                                                   | 161 ms: 1.02x faster                                                         |
| nbody          | 39.8 ms                                                                  | 40.1 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7+-0adc728 | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 99.6 ms                                                                  | 94.3 ms: 1.06x faster                                                        |
| regex_compile  | 41.5 ms                                                                  | 39.5 ms: 1.05x faster                                                        |
| regex_v8       | 9.97 ms                                                                  | 9.57 ms: 1.04x faster                                                        |
| regex_effbot   | 1.49 ms                                                                  | 1.46 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7+-0adc728 | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_process    | 22.7 ms                                                                  | 21.3 ms: 1.07x faster                                                        |
| json_loads           | 10.7 us                                                                  | 10.4 us: 1.04x faster                                                        |
| tomli_loads          | 648 ms                                                                   | 630 ms: 1.03x faster                                                         |
| unpickle_pure_python | 85.9 us                                                                  | 84.2 us: 1.02x faster                                                        |
| json_dumps           | 3.56 ms                                                                  | 3.51 ms: 1.01x faster                                                        |
| xml_etree_generate   | 31.9 ms                                                                  | 31.5 ms: 1.01x faster                                                        |
| pickle_pure_python   | 127 us                                                                   | 125 us: 1.01x faster                                                         |
| xml_etree_parse      | 61.2 ms                                                                  | 63.0 ms: 1.03x slower                                                        |
| Geometric mean       | (ref)                                                                    | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7+-0adc728 | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.84 ms                                                                  | 8.71 ms: 1.01x faster                                                        |
| python_startup_no_site | 6.35 ms                                                                  | 6.26 ms: 1.01x faster                                                        |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7+-0adc728 | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 14.1 ms                                                                  | 12.5 ms: 1.14x faster                                                        |
| mako            | 3.99 ms                                                                  | 3.97 ms: 1.01x faster                                                        |
| Geometric mean  | (ref)                                                                    | 1.07x faster                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7+-0adc728 | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| logging_format                   | 2.41 us                                                                  | 1.90 us: 1.27x faster                                                        |
| logging_simple                   | 2.22 us                                                                  | 1.76 us: 1.26x faster                                                        |
| coroutines                       | 10.9 ms                                                                  | 9.15 ms: 1.19x faster                                                        |
| django_template                  | 14.1 ms                                                                  | 12.5 ms: 1.14x faster                                                        |
| async_tree_io                    | 232 ms                                                                   | 207 ms: 1.12x faster                                                         |
| sqlglot_v2_normalize             | 46.7 ms                                                                  | 42.8 ms: 1.09x faster                                                        |
| many_optionals                   | 245 us                                                                   | 225 us: 1.09x faster                                                         |
| async_tree_none_tg               | 99.0 ms                                                                  | 90.9 ms: 1.09x faster                                                        |
| async_tree_none                  | 97.2 ms                                                                  | 89.5 ms: 1.09x faster                                                        |
| async_tree_eager_io              | 223 ms                                                                   | 205 ms: 1.09x faster                                                         |
| async_tree_io_tg                 | 226 ms                                                                   | 208 ms: 1.08x faster                                                         |
| generators                       | 19.0 ms                                                                  | 17.5 ms: 1.08x faster                                                        |
| async_tree_eager_io_tg           | 220 ms                                                                   | 203 ms: 1.08x faster                                                         |
| deltablue                        | 1.20 ms                                                                  | 1.11 ms: 1.08x faster                                                        |
| mdp                              | 549 ms                                                                   | 511 ms: 1.08x faster                                                         |
| async_generators                 | 191 ms                                                                   | 178 ms: 1.08x faster                                                         |
| 2to3                             | 119 ms                                                                   | 111 ms: 1.07x faster                                                         |
| sqlglot_v2_transpile             | 590 us                                                                   | 551 us: 1.07x faster                                                         |
| async_tree_eager_tg              | 82.5 ms                                                                  | 77.2 ms: 1.07x faster                                                        |
| sqlglot_v2_optimize              | 22.5 ms                                                                  | 21.1 ms: 1.07x faster                                                        |
| xml_etree_process                | 22.7 ms                                                                  | 21.3 ms: 1.07x faster                                                        |
| html5lib                         | 20.4 ms                                                                  | 19.2 ms: 1.06x faster                                                        |
| scimark_sor                      | 39.4 ms                                                                  | 37.1 ms: 1.06x faster                                                        |
| dulwich_log                      | 19.0 ms                                                                  | 17.9 ms: 1.06x faster                                                        |
| async_tree_memoization_tg        | 136 ms                                                                   | 129 ms: 1.06x faster                                                         |
| async_tree_memoization           | 134 ms                                                                   | 127 ms: 1.06x faster                                                         |
| regex_dna                        | 99.6 ms                                                                  | 94.3 ms: 1.06x faster                                                        |
| sqlglot_v2_parse                 | 464 us                                                                   | 439 us: 1.06x faster                                                         |
| sympy_expand                     | 173 ms                                                                   | 164 ms: 1.05x faster                                                         |
| regex_compile                    | 41.5 ms                                                                  | 39.5 ms: 1.05x faster                                                        |
| docutils                         | 1.01 sec                                                                 | 963 ms: 1.05x faster                                                         |
| chaos                            | 22.2 ms                                                                  | 21.3 ms: 1.05x faster                                                        |
| typing_runtime_protocols         | 64.9 us                                                                  | 62.1 us: 1.05x faster                                                        |
| async_tree_eager_memoization_tg  | 121 ms                                                                   | 116 ms: 1.05x faster                                                         |
| regex_v8                         | 9.97 ms                                                                  | 9.57 ms: 1.04x faster                                                        |
| thrift                           | 313 us                                                                   | 300 us: 1.04x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 250 ms                                                                   | 241 ms: 1.04x faster                                                         |
| async_tree_cpu_io_mixed          | 249 ms                                                                   | 240 ms: 1.04x faster                                                         |
| subparsers                       | 3.64 ms                                                                  | 3.52 ms: 1.04x faster                                                        |
| json_loads                       | 10.7 us                                                                  | 10.4 us: 1.04x faster                                                        |
| scimark_sparse_mat_mult          | 1.84 ms                                                                  | 1.78 ms: 1.03x faster                                                        |
| async_tree_eager                 | 37.5 ms                                                                  | 36.3 ms: 1.03x faster                                                        |
| sphinx                           | 400 ms                                                                   | 388 ms: 1.03x faster                                                         |
| pycparser                        | 456 ms                                                                   | 442 ms: 1.03x faster                                                         |
| async_tree_eager_memoization     | 104 ms                                                                   | 101 ms: 1.03x faster                                                         |
| tomli_loads                      | 648 ms                                                                   | 630 ms: 1.03x faster                                                         |
| bench_mp_pool                    | 45.6 ms                                                                  | 44.3 ms: 1.03x faster                                                        |
| deepcopy                         | 96.1 us                                                                  | 93.4 us: 1.03x faster                                                        |
| hexiom                           | 2.46 ms                                                                  | 2.39 ms: 1.03x faster                                                        |
| scimark_monte_carlo              | 23.3 ms                                                                  | 22.7 ms: 1.03x faster                                                        |
| pprint_safe_repr                 | 257 ms                                                                   | 251 ms: 1.03x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 241 ms                                                                   | 235 ms: 1.03x faster                                                         |
| raytrace                         | 113 ms                                                                   | 111 ms: 1.03x faster                                                         |
| pprint_pformat                   | 521 ms                                                                   | 509 ms: 1.02x faster                                                         |
| regex_effbot                     | 1.49 ms                                                                  | 1.46 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 218 ms                                                                   | 212 ms: 1.02x faster                                                         |
| gc_traversal                     | 2.07 ms                                                                  | 2.02 ms: 1.02x faster                                                        |
| pidigits                         | 165 ms                                                                   | 161 ms: 1.02x faster                                                         |
| coverage                         | 33.4 ms                                                                  | 32.7 ms: 1.02x faster                                                        |
| json                             | 1.85 ms                                                                  | 1.82 ms: 1.02x faster                                                        |
| unpickle_pure_python             | 85.9 us                                                                  | 84.2 us: 1.02x faster                                                        |
| bpe_tokeniser                    | 1.80 sec                                                                 | 1.77 sec: 1.02x faster                                                       |
| deepcopy_reduce                  | 1.01 us                                                                  | 994 ns: 1.02x faster                                                         |
| create_gc_cycles                 | 921 us                                                                   | 904 us: 1.02x faster                                                         |
| asyncio_websockets               | 188 ms                                                                   | 185 ms: 1.02x faster                                                         |
| scimark_lu                       | 28.6 ms                                                                  | 28.2 ms: 1.02x faster                                                        |
| pathlib                          | 10.8 ms                                                                  | 10.6 ms: 1.02x faster                                                        |
| python_startup                   | 8.84 ms                                                                  | 8.71 ms: 1.01x faster                                                        |
| json_dumps                       | 3.56 ms                                                                  | 3.51 ms: 1.01x faster                                                        |
| telco                            | 2.60 ms                                                                  | 2.56 ms: 1.01x faster                                                        |
| sympy_sum                        | 56.4 ms                                                                  | 55.6 ms: 1.01x faster                                                        |
| python_startup_no_site           | 6.35 ms                                                                  | 6.26 ms: 1.01x faster                                                        |
| go                               | 46.9 ms                                                                  | 46.3 ms: 1.01x faster                                                        |
| xml_etree_generate               | 31.9 ms                                                                  | 31.5 ms: 1.01x faster                                                        |
| meteor_contest                   | 45.9 ms                                                                  | 45.4 ms: 1.01x faster                                                        |
| sqlite_synth                     | 949 ns                                                                   | 939 ns: 1.01x faster                                                         |
| crypto_pyaes                     | 32.0 ms                                                                  | 31.7 ms: 1.01x faster                                                        |
| logging_silent                   | 34.8 ns                                                                  | 34.4 ns: 1.01x faster                                                        |
| pickle_pure_python               | 127 us                                                                   | 125 us: 1.01x faster                                                         |
| scimark_fft                      | 97.9 ms                                                                  | 97.0 ms: 1.01x faster                                                        |
| pyflate                          | 148 ms                                                                   | 147 ms: 1.01x faster                                                         |
| mako                             | 3.99 ms                                                                  | 3.97 ms: 1.01x faster                                                        |
| bench_thread_pool                | 431 us                                                                   | 429 us: 1.01x faster                                                         |
| spectral_norm                    | 37.8 ms                                                                  | 37.7 ms: 1.00x faster                                                        |
| k_core                           | 859 ms                                                                   | 857 ms: 1.00x faster                                                         |
| nbody                            | 39.8 ms                                                                  | 40.1 ms: 1.01x slower                                                        |
| nqueens                          | 32.2 ms                                                                  | 32.4 ms: 1.01x slower                                                        |
| xml_etree_parse                  | 61.2 ms                                                                  | 63.0 ms: 1.03x slower                                                        |
| richards_super                   | 11.2 ms                                                                  | 11.5 ms: 1.03x slower                                                        |
| richards                         | 9.37 ms                                                                  | 9.83 ms: 1.05x slower                                                        |
| comprehensions                   | 5.89 us                                                                  | 7.33 us: 1.24x slower                                                        |
| Geometric mean                   | (ref)                                                                    | 1.04x faster                                                                 |

Benchmark hidden because not significant (10): pylint, deepcopy_memo, fannkuch, sympy_integrate, float, connected_components, shortest_path, dask, xml_etree_iterparse, sympy_str

- Geometric mean (including insignificant results): 1.037x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.01x