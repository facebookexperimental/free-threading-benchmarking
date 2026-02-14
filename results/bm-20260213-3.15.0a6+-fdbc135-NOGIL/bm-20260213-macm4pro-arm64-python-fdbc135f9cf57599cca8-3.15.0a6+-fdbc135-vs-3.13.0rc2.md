# Results vs. 3.13.0rc2

- fork: python
- ref: fdbc135f9cf57599cca8
- machine: darwin-arm64
- commit hash: fdbc135
- commit date: 2026-02-13
- overall geometric mean: 1.014x faster
- HPT reliability: 53.40%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 423 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 242 ms: 2.15x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.14x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 238 ms: 1.70x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| async_generators                 | 193 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.2 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.20x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.1 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.4 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.6 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.0 ms: 1.18x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.95 ms: 1.18x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 871 ms: 1.15x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.83 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.13 ms: 1.20x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.7 ms: 1.06x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 12.3 ms: 1.23x slower                                                    |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| mako            | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 805 us: 2.53x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 242 ms: 2.15x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.14x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 507 us: 1.96x faster                                                     |
| mdp                              | 1.06 sec                                                       | 610 ms: 1.73x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 238 ms: 1.70x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.15 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 986 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 106 us: 1.36x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.31x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| go                               | 72.6 ms                                                        | 59.7 ms: 1.21x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 789 ns: 1.20x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.0 ms: 1.18x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.2 ms: 1.18x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.95 ms: 1.18x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 871 ms: 1.15x faster                                                     |
| pyflate                          | 222 ms                                                         | 193 ms: 1.15x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| float                            | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.06x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.04 sec: 1.05x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                    |
| async_generators                 | 193 ms                                                         | 189 ms: 1.02x faster                                                     |
| pycparser                        | 470 ms                                                         | 461 ms: 1.02x faster                                                     |
| fannkuch                         | 179 ms                                                         | 176 ms: 1.02x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 528 ms: 1.00x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 325 ms: 1.01x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 661 ms: 1.02x slower                                                     |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 423 ms: 1.03x slower                                                     |
| richards                         | 22.1 ms                                                        | 22.9 ms: 1.04x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.6 ms: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.2 ms: 1.06x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.7 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.10 ms: 1.08x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.41 us: 1.08x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.4 ms: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.1 ns: 1.09x slower                                                    |
| thrift                           | 309 us                                                         | 336 us: 1.09x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.09x slower                                                     |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.67 us: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.2 ms: 1.09x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 72.3 us: 1.12x slower                                                    |
| shortest_path                    | 225 ms                                                         | 252 ms: 1.12x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.13x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 42.4 ms: 1.14x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.83 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.2 ms: 1.15x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.0 ms: 1.15x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.8 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.8 ms: 1.16x slower                                                    |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| raytrace                         | 109 ms                                                         | 129 ms: 1.19x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.13 ms: 1.20x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 192 ms: 1.20x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.20x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.16 ms: 1.22x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.29 us: 1.22x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 12.3 ms: 1.23x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.7 ms: 1.24x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.1 ms: 1.24x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 43.3 ms: 1.29x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.4 ms: 1.33x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 551 us: 1.34x slower                                                     |
| generators                       | 15.7 ms                                                        | 21.1 ms: 1.35x slower                                                    |
| many_optionals                   | 200 us                                                         | 270 us: 1.35x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 58.1 ms: 1.36x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.1 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): regex_dna
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260213-3.15.0a6+-fdbc135-NOGIL/bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.014x faster

# HPT report

- Reliability score: 53.40% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x