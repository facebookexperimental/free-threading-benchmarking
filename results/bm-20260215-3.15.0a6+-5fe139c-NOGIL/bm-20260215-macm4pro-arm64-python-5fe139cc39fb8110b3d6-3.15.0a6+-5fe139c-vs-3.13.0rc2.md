# Results vs. 3.13.0rc2

- fork: python
- ref: 5fe139cc39fb8110b3d6
- machine: darwin-arm64
- commit hash: 5fe139c
- commit date: 2026-02-15
- overall geometric mean: 1.012x faster
- HPT reliability: 57.51%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| sphinx         | 409 ms                                                         | 422 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 244 ms: 2.14x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.12x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 249 ms: 1.55x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 270 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| async_generators                 | 193 ms                                                         | 189 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 227 ms: 1.01x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.7 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.20x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.5 ms: 3.23x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.2 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.2 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 50.9 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.97 ms: 1.17x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 884 ms: 1.13x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.85 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.14 ms: 1.20x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.8 ms: 1.06x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                    |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| mako            | 4.41 ms                                                        | 5.60 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 817 us: 2.50x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 244 ms: 2.14x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.12x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 519 us: 1.91x faster                                                     |
| mdp                              | 1.06 sec                                                       | 603 ms: 1.75x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 249 ms: 1.55x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.19 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 991 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 106 us: 1.37x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.32x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                    |
| go                               | 72.6 ms                                                        | 60.7 ms: 1.20x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 793 ns: 1.20x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.97 ms: 1.17x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.0 ms: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                     |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 884 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 270 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| float                            | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.06x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.04 sec: 1.04x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| fannkuch                         | 179 ms                                                         | 173 ms: 1.03x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                    |
| async_generators                 | 193 ms                                                         | 189 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| pycparser                        | 470 ms                                                         | 465 ms: 1.01x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.2 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 529 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 227 ms: 1.01x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 327 ms: 1.02x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.02x slower                                                     |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 667 ms: 1.03x slower                                                     |
| sphinx                           | 409 ms                                                         | 422 ms: 1.03x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.3 ms: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.9 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.8 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.12 ms: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.7 ms: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.0 ns: 1.08x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.44 us: 1.09x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.7 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.70 us: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.7 ms: 1.10x slower                                                    |
| thrift                           | 309 us                                                         | 341 us: 1.10x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                    |
| shortest_path                    | 225 ms                                                         | 253 ms: 1.12x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 72.8 us: 1.13x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.85 ms: 1.14x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 42.6 ms: 1.14x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.66 ms: 1.15x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.9 ms: 1.15x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.6 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 61.2 ms: 1.17x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.3 ms: 1.17x slower                                                    |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| raytrace                         | 109 ms                                                         | 128 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.13 ms: 1.20x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.14 ms: 1.20x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.20x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.35 us: 1.23x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.8 ms: 1.24x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.3 ms: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.60 ms: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 43.3 ms: 1.29x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 56.5 ms: 1.32x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 551 us: 1.34x slower                                                     |
| nbody                            | 42.5 ms                                                        | 57.2 ms: 1.35x slower                                                    |
| generators                       | 15.7 ms                                                        | 21.2 ms: 1.35x slower                                                    |
| many_optionals                   | 200 us                                                         | 272 us: 1.36x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.5 ms: 3.23x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260215-3.15.0a6+-5fe139c-NOGIL/bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 57.51% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x