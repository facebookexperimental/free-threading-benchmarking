# Results vs. 3.13.0rc2

- fork: python
- ref: 40095d526bd8ddbabee0
- machine: darwin-arm64
- commit hash: 40095d5
- commit date: 2026-03-15
- overall geometric mean: 1.017x faster
- HPT reliability: 61.25%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| docutils       | 1.05 sec                                                       | 994 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 424 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 240 ms: 2.17x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.13x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 237 ms: 1.71x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_generators                 | 193 ms                                                         | 190 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.6 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.2 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                     |
| nbody          | 42.5 ms                                                        | 56.8 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.6 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 50.2 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.90 ms: 1.19x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.7 ms: 1.19x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 843 ms: 1.19x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 106 us: 1.06x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.88 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.18 ms: 1.21x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.7 ms: 1.06x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.13x slower                                                    |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| mako            | 4.41 ms                                                        | 5.54 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 817 us: 2.50x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 240 ms: 2.17x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.13x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 510 us: 1.95x faster                                                     |
| mdp                              | 1.06 sec                                                       | 609 ms: 1.74x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 237 ms: 1.71x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.08 ms: 1.53x faster                                                    |
| k_core                           | 1.46 sec                                                       | 994 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 107 us: 1.36x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.31x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| go                               | 72.6 ms                                                        | 59.8 ms: 1.21x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 793 ns: 1.19x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.90 ms: 1.19x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.7 ms: 1.19x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 843 ms: 1.19x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.4 ms: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| float                            | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| docutils                         | 1.05 sec                                                       | 994 ms: 1.05x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| pycparser                        | 470 ms                                                         | 460 ms: 1.02x faster                                                     |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                    |
| async_generators                 | 193 ms                                                         | 190 ms: 1.01x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                     |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.6 ms: 1.01x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 329 ms: 1.02x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 672 ms: 1.03x slower                                                     |
| sphinx                           | 409 ms                                                         | 424 ms: 1.04x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.0 ms: 1.04x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.2 ms: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.36 us: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.7 ms: 1.06x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 106 us: 1.06x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 26.3 ms: 1.07x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.5 ns: 1.07x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.64 us: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.6 ms: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.14 ms: 1.08x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.6 ms: 1.09x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.7 ms: 1.09x slower                                                    |
| thrift                           | 309 us                                                         | 341 us: 1.10x slower                                                     |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| chaos                            | 24.3 ms                                                        | 27.1 ms: 1.12x slower                                                    |
| shortest_path                    | 225 ms                                                         | 252 ms: 1.12x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 72.7 us: 1.12x slower                                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.12x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.20 ms: 1.13x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.14x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.88 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 51.2 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 56.1 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.5 ms: 1.18x slower                                                    |
| connected_components             | 208 ms                                                         | 244 ms: 1.18x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 192 ms: 1.20x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.18 ms: 1.21x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.15 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.24 us: 1.21x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.5 ms: 1.23x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.1 ms: 1.24x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.54 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.25x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 54.3 ms: 1.27x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.5 ms: 1.30x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 44.3 ms: 1.32x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.8 ms: 1.34x slower                                                    |
| many_optionals                   | 200 us                                                         | 269 us: 1.34x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 583 us: 1.42x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.2 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260315-3.15.0a7+-40095d5-NOGIL/bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.017x faster

# HPT report

- Reliability score: 61.25% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x