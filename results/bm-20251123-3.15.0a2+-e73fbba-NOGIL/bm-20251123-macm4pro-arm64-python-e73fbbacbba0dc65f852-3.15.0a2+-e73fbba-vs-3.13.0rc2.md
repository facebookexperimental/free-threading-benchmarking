# Results vs. 3.13.0rc2

- fork: python
- ref: e73fbbacbba0dc65f852
- machine: darwin-arm64
- commit hash: e73fbba
- commit date: 2025-11-23
- overall geometric mean: 1.026x faster
- HPT reliability: 58.93%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.08x slower                                                     |
| docutils       | 1.05 sec                                                       | 987 ms: 1.06x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 190 ms: 2.74x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 199 ms: 2.63x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.06x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.87x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 84.9 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 122 ms: 1.52x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 97.9 ms: 1.45x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.44x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.6 ms: 2.65x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.4 ms: 1.15x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 55.5 ms: 1.31x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.21 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.7 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 36.7 ms: 1.26x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 871 ms: 1.15x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 56.3 ms: 1.11x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.1 ms: 1.01x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.03x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.2 ms: 1.03x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.71 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.05 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.0 ms: 1.08x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                    |
| mako            | 4.41 ms                                                        | 5.52 ms: 1.25x slower                                                    |
| django_template | 12.5 ms                                                        | 15.8 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 190 ms: 2.74x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 199 ms: 2.63x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 779 us: 2.62x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.06x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 496 us: 2.00x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.87x faster                                                     |
| mdp                              | 1.06 sec                                                       | 602 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 84.9 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 122 ms: 1.52x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 97.9 ms: 1.45x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.44x faster                                                     |
| deepcopy                         | 145 us                                                         | 108 us: 1.35x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.29x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.7 ms: 1.26x faster                                                    |
| go                               | 72.6 ms                                                        | 58.7 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.8 ms: 1.17x faster                                                    |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.21 ms: 1.16x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 825 ns: 1.15x faster                                                     |
| float                            | 31.4 ms                                                        | 27.4 ms: 1.15x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 871 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 56.3 ms: 1.11x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.19 us: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                   |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| docutils                         | 1.05 sec                                                       | 987 ms: 1.06x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 169 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.97 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| pycparser                        | 470 ms                                                         | 462 ms: 1.02x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.1 ms: 1.01x slower                                                    |
| richards                         | 22.1 ms                                                        | 22.6 ms: 1.02x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.03x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.2 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 334 ms: 1.04x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 684 ms: 1.05x slower                                                     |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 26.1 ms: 1.06x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.7 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.02 ms: 1.07x slower                                                    |
| dask                             | 525 ms                                                         | 562 ms: 1.07x slower                                                     |
| thrift                           | 309 us                                                         | 331 us: 1.07x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 23.0 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.07 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| 2to3                             | 112 ms                                                         | 121 ms: 1.08x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.43 us: 1.09x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.58 ms: 1.09x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.68 us: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 44.7 ns: 1.10x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.4 us: 1.10x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.2 ms: 1.11x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.71 ms: 1.12x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.6 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.0 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.3 ms: 1.15x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.6 ms: 1.16x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.2 ms: 1.16x slower                                                    |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.05 ms: 1.18x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.09 us: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.8 ms: 1.21x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.24x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.22 ms: 1.25x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.52 ms: 1.25x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.1 ms: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.8 ms: 1.26x slower                                                    |
| coverage                         | 31.2 ms                                                        | 39.5 ms: 1.26x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 54.4 ms: 1.27x slower                                                    |
| nbody                            | 42.5 ms                                                        | 55.5 ms: 1.31x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 561 us: 1.36x slower                                                     |
| many_optionals                   | 200 us                                                         | 383 us: 1.91x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.6 ms: 2.65x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.9 ms: 3.02x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (2): sphinx, regex_dna
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251123-3.15.0a2+-e73fbba-NOGIL/bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.026x faster

# HPT report

- Reliability score: 58.93% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.32x