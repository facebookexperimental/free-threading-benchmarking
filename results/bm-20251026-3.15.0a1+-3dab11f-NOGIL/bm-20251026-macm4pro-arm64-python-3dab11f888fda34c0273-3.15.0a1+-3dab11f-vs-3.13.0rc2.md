# Results vs. 3.13.0rc2

- fork: python
- ref: 3dab11f888fda34c0273
- machine: darwin-arm64
- commit hash: 3dab11f
- commit date: 2025-10-26
- overall geometric mean: 1.001x faster
- HPT reliability: 77.33%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                    |
| sphinx         | 409 ms                                                         | 416 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.03x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 87.2 ms: 1.52x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.49x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.41x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 11.2 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 49.3 ms: 1.14x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.6 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.0 ms: 1.05x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 61.6 ms: 1.45x slower                                                    |
| Geometric mean | (ref)                                                          | 1.11x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.38 ms: 1.14x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 53.6 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 36.9 ms: 1.25x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.05 ms: 1.15x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 56.6 ms: 1.10x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 978 ms: 1.02x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 154 us: 1.18x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.69 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.07 ms: 1.19x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.6 ms: 1.15x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.9 ms: 1.19x slower                                                    |
| mako            | 4.41 ms                                                        | 5.78 ms: 1.31x slower                                                    |
| django_template | 12.5 ms                                                        | 16.8 ms: 1.34x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.25x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 763 us: 2.68x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 472 us: 2.11x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.03x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                     |
| mdp                              | 1.06 sec                                                       | 605 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 87.2 ms: 1.52x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.49x faster                                                     |
| k_core                           | 1.46 sec                                                       | 996 ms: 1.47x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.41x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.1 us: 1.25x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.9 ms: 1.25x faster                                                    |
| deepcopy                         | 145 us                                                         | 118 us: 1.23x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.2 ms: 1.16x faster                                                    |
| go                               | 72.6 ms                                                        | 62.6 ms: 1.16x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.05 ms: 1.15x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.38 ms: 1.14x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 833 ns: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| pyflate                          | 222 ms                                                         | 201 ms: 1.10x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 56.6 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                   |
| float                            | 31.4 ms                                                        | 30.0 ms: 1.05x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.2 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.26 us: 1.02x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 978 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 530 ms: 1.01x slower                                                     |
| telco                            | 3.07 ms                                                        | 3.10 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 416 ms: 1.02x slower                                                     |
| pycparser                        | 470 ms                                                         | 478 ms: 1.02x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                    |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.02x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.2 ms: 1.04x slower                                                    |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                     |
| fannkuch                         | 179 ms                                                         | 186 ms: 1.04x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.05 ms: 1.07x slower                                                    |
| connected_components             | 208 ms                                                         | 222 ms: 1.07x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 134 ms: 1.08x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.09x slower                                                     |
| richards                         | 22.1 ms                                                        | 24.2 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 355 ms: 1.10x slower                                                     |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| thrift                           | 309 us                                                         | 343 us: 1.11x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 723 ms: 1.11x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 27.5 ms: 1.12x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 53.6 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 42.4 ms: 1.12x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.69 ms: 1.12x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 45.8 ns: 1.13x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.21 ms: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.53 us: 1.13x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.3 ms: 1.14x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.3 ms: 1.15x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.81 us: 1.15x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 74.4 us: 1.15x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 24.6 ms: 1.15x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.0 ms: 1.17x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 51.1 ms: 1.17x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 154 us: 1.18x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 44.2 ms: 1.19x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.07 ms: 1.19x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.9 ms: 1.19x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 57.6 ms: 1.20x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.6 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.2 ms: 1.22x slower                                                    |
| raytrace                         | 109 ms                                                         | 134 ms: 1.23x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.21 ms: 1.24x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.52 us: 1.25x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 43.1 ms: 1.28x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 55.1 ms: 1.29x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.8 ms: 1.31x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.78 ms: 1.31x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 551 us: 1.34x slower                                                     |
| django_template                  | 12.5 ms                                                        | 16.8 ms: 1.34x slower                                                    |
| nbody                            | 42.5 ms                                                        | 61.6 ms: 1.45x slower                                                    |
| many_optionals                   | 200 us                                                         | 386 us: 1.93x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.6 ms: 2.72x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 19.0 ms: 3.04x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (1): regex_dna
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251026-3.15.0a1+-3dab11f-NOGIL/bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 77.33% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x