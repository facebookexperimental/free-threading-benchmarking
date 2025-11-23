# Results vs. 3.12.6

- fork: python
- ref: e73fbbacbba0dc65f852
- machine: darwin-arm64
- commit hash: e73fbba
- commit date: 2025-11-23
- overall geometric mean: 1.142x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| html5lib       | 23.0 ms                                                  | 22.0 ms: 1.05x faster                                                    |
| sphinx         | 434 ms                                                   | 392 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 226 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.15x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 227 ms: 2.02x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.7 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.6 ms: 1.76x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.3 ms: 1.10x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 124 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.7 ms: 2.51x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.32x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.4 ms: 1.44x faster                                                    |
| nbody          | 54.2 ms                                                  | 45.6 ms: 1.19x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                    | 1.19x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.2 ms: 1.18x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.6 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.1 ms: 1.32x faster                                                    |
| tomli_loads          | 957 ms                                                   | 840 ms: 1.14x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 60.3 ms: 1.13x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.6 ms: 1.12x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.89 ms: 1.09x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.5 us: 1.06x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.02x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.82 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.91 ms: 1.06x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.2 ms: 1.03x faster                                                    |
| mako            | 4.77 ms                                                  | 4.69 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 226 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.15x faster                                                     |
| mdp                              | 1.09 sec                                                 | 535 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 227 ms: 2.02x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.7 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.6 ms: 1.76x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.2 us: 1.63x faster                                                    |
| deepcopy                         | 161 us                                                   | 101 us: 1.60x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| float                            | 37.9 ms                                                  | 26.4 ms: 1.44x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.17 us: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.08 us: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| go                               | 70.0 ms                                                  | 52.8 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.1 ms: 1.32x faster                                                    |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 42.6 ms: 1.27x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.2 ms: 1.24x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.2 ns: 1.24x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 116 ms: 1.23x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| nbody                            | 54.2 ms                                                  | 45.6 ms: 1.19x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.6 ms: 1.18x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.2 ms: 1.18x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.5 ms: 1.18x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.76 ms: 1.18x faster                                                    |
| pylint                           | 128 ms                                                   | 109 ms: 1.17x faster                                                     |
| pyflate                          | 216 ms                                                   | 184 ms: 1.17x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.0 ms: 1.15x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 44.7 ms: 1.15x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.46 us: 1.14x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 840 ms: 1.14x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.3 ms: 1.13x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.6 ms: 1.12x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.6 ms: 1.12x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.8 ms: 1.12x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.3 us: 1.12x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.1 ms: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 392 ms: 1.11x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.3 ms: 1.10x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.89 ms: 1.09x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.78 ms: 1.09x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 458 ms: 1.09x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.40 ms: 1.08x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.91 ms: 1.06x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 97.5 us: 1.06x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 634 ms: 1.05x faster                                                     |
| thrift                           | 322 us                                                   | 307 us: 1.05x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.0 ms: 1.05x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 313 ms: 1.05x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 95.6 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.2 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.2 ms: 1.03x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.69 ms: 1.02x faster                                                    |
| fannkuch                         | 176 ms                                                   | 173 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 959 ns: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.04 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 427 us: 1.02x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 171 ms: 1.02x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.02x slower                                                    |
| dask                             | 528 ms                                                   | 541 ms: 1.03x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.8 ms: 1.04x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 909 us: 1.10x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 43.7 ms: 1.10x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.82 ms: 1.10x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.88 ms: 1.10x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 124 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| coverage                         | 26.9 ms                                                  | 34.2 ms: 1.27x slower                                                    |
| many_optionals                   | 195 us                                                   | 355 us: 1.82x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.7 ms: 2.51x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                             |

Benchmark hidden because not significant (2): pickle_pure_python, regex_v8
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251123-3.15.0a2+-e73fbba/bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.142x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.23x