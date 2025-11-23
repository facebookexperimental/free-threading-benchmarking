# Results vs. 3.12.6

- fork: python
- ref: e73fbbacbba0dc65f852
- machine: darwin-arm64
- commit hash: e73fbba
- commit date: 2025-11-23
- overall geometric mean: 1.112x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| docutils       | 1.02 sec                                                 | 987 ms: 1.04x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 406 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 199 ms: 2.49x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.44x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 190 ms: 2.34x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 207 ms: 2.22x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 84.9 ms: 2.03x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 122 ms: 1.89x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 97.9 ms: 1.82x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 128 ms: 1.74x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.7 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.6 ms: 2.38x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.39x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.4 ms: 1.38x faster                                                    |
| nbody          | 54.2 ms                                                  | 55.5 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.7 ms: 1.08x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.21 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 36.7 ms: 1.41x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.3 ms: 1.21x faster                                                    |
| tomli_loads          | 957 ms                                                   | 871 ms: 1.10x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.94 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.1 ms: 1.08x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.2 ms: 1.02x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.71 ms: 1.21x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.05 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.0 ms: 1.05x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| mako            | 4.77 ms                                                  | 5.52 ms: 1.16x slower                                                    |
| django_template | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.11x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 779 us: 2.58x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 199 ms: 2.49x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.44x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 190 ms: 2.34x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 207 ms: 2.22x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 84.9 ms: 2.03x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 122 ms: 1.89x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 97.9 ms: 1.82x faster                                                    |
| mdp                              | 1.09 sec                                                 | 602 ms: 1.81x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 128 ms: 1.74x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 496 us: 1.67x faster                                                     |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.7 ms: 1.41x faster                                                    |
| float                            | 37.9 ms                                                  | 27.4 ms: 1.38x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.19 us: 1.23x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.09 us: 1.22x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 56.3 ms: 1.21x faster                                                    |
| go                               | 70.0 ms                                                  | 58.7 ms: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 825 ns: 1.17x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| pylint                           | 128 ms                                                   | 111 ms: 1.15x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 44.7 ns: 1.14x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                     |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.4 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.8 ms: 1.11x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 18.9 ms: 1.10x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 871 ms: 1.10x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.58 ms: 1.09x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.94 ms: 1.08x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 50.7 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 462 ms: 1.08x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 36.1 ms: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.6 ms: 1.07x faster                                                    |
| sphinx                           | 434 ms                                                   | 406 ms: 1.07x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.43 us: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.6 ms: 1.05x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.68 us: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.21 ms: 1.04x faster                                                    |
| fannkuch                         | 176 ms                                                   | 169 ms: 1.04x faster                                                     |
| docutils                         | 1.02 sec                                                 | 987 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 26.2 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| richards                         | 22.4 ms                                                  | 22.6 ms: 1.01x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.07 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 334 ms: 1.02x slower                                                     |
| nbody                            | 54.2 ms                                                  | 55.5 ms: 1.02x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.7 ms: 1.02x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.1 ms: 1.03x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 684 ms: 1.03x slower                                                     |
| thrift                           | 322 us                                                   | 331 us: 1.03x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.2 ms: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.3 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.0 ms: 1.05x slower                                                    |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 54.4 ms: 1.06x slower                                                    |
| dask                             | 528 ms                                                   | 562 ms: 1.06x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.22 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.1 ms: 1.08x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.12x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.97 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.0 ms: 1.15x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.8 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.52 ms: 1.16x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.71 ms: 1.21x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.05 ms: 1.24x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 561 us: 1.34x slower                                                     |
| coverage                         | 26.9 ms                                                  | 39.5 ms: 1.47x slower                                                    |
| many_optionals                   | 195 us                                                   | 383 us: 1.96x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.6 ms: 2.38x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (4): nqueens, sympy_integrate, pidigits, typing_runtime_protocols
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251123-3.15.0a2+-e73fbba-NOGIL/bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.112x faster

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.37x