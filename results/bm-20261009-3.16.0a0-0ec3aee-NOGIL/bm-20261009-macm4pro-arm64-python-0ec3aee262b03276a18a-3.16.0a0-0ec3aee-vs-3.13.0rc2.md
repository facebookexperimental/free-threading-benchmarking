# Results vs. 3.13.0rc2

- fork: python
- ref: 0ec3aee262b03276a18a
- machine: darwin-arm64
- commit hash: 0ec3aee
- commit date: 2026-10-09
- overall geometric mean: 1.019x slower
- HPT reliability: 93.80%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 127 ms: 1.14x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                   |
| sphinx         | 409 ms                                                         | 446 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 290 ms: 1.80x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 293 ms: 1.79x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 294 ms: 1.38x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 303 ms: 1.27x faster                                                    |
| async_generators                 | 193 ms                                                         | 160 ms: 1.21x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 289 ms: 1.04x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 181 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 230 ms: 1.02x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 125 ms: 1.02x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 140 ms: 1.06x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.7 ms: 1.15x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 12.5 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 270 ms: 1.30x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 162 ms: 1.58x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 113 ms: 3.91x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (3): async_tree_none, async_tree_cpu_io_mixed, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| float          | 31.4 ms                                                        | 32.8 ms: 1.05x slower                                                   |
| nbody          | 42.5 ms                                                        | 59.6 ms: 1.40x slower                                                   |
| Geometric mean | (ref)                                                          | 1.13x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.34 ms: 1.21x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.3 ms: 1.03x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 64.1 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 876 ms: 1.14x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.8 ms: 1.10x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.08x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 38.8 ms: 1.08x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 29.7 ms: 1.17x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 155 us: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.34 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.20x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.76 ms: 1.30x slower                                                   |
| django_template | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.33x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 772 us: 2.64x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 485 us: 2.05x faster                                                    |
| pylint                           | 106 ms                                                         | 53.5 ms: 1.98x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 290 ms: 1.80x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 293 ms: 1.79x faster                                                    |
| mdp                              | 1.06 sec                                                       | 595 ms: 1.78x faster                                                    |
| k_core                           | 1.46 sec                                                       | 994 ms: 1.47x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.30 ms: 1.46x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 294 ms: 1.38x faster                                                    |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 303 ms: 1.27x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                   |
| async_generators                 | 193 ms                                                         | 160 ms: 1.21x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.34 ms: 1.21x faster                                                   |
| go                               | 72.6 ms                                                        | 60.7 ms: 1.19x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 803 ns: 1.18x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 14.4 us: 1.14x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 876 ms: 1.14x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 57.3 us: 1.13x faster                                                   |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 57.6 ms: 1.11x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.8 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                  |
| deepcopy_reduce                  | 1.30 us                                                        | 1.20 us: 1.08x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 289 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.3 ms: 1.03x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 181 ms: 1.03x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 92.3 ms: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| fannkuch                         | 179 ms                                                         | 176 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                    |
| pycparser                        | 470 ms                                                         | 477 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 230 ms: 1.02x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 125 ms: 1.02x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.16 ms: 1.03x slower                                                   |
| float                            | 31.4 ms                                                        | 32.8 ms: 1.05x slower                                                   |
| async_tree_none_tg               | 133 ms                                                         | 140 ms: 1.06x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.08x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 38.8 ms: 1.08x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.18 ms: 1.09x slower                                                   |
| sphinx                           | 409 ms                                                         | 446 ms: 1.09x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 354 ms: 1.10x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.3 ms: 1.10x slower                                                   |
| shortest_path                    | 225 ms                                                         | 249 ms: 1.11x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.49 us: 1.11x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.74 us: 1.12x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.5 ms: 1.12x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.7 ms: 1.12x slower                                                   |
| thrift                           | 309 us                                                         | 347 us: 1.12x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 49.3 ms: 1.13x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 736 ms: 1.13x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.24 ms: 1.14x slower                                                   |
| 2to3                             | 112 ms                                                         | 127 ms: 1.14x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 42.7 ms: 1.15x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.7 ms: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.6 ms: 1.15x slower                                                   |
| connected_components             | 208 ms                                                         | 240 ms: 1.15x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 12.5 ms: 1.17x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.08 ms: 1.17x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.3 ms: 1.17x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 29.7 ms: 1.17x slower                                                   |
| chaos                            | 24.3 ms                                                        | 28.8 ms: 1.18x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 155 us: 1.19x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 41.2 ms: 1.22x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 49.8 ns: 1.23x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.34 ms: 1.23x slower                                                   |
| raytrace                         | 109 ms                                                         | 135 ms: 1.24x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.46 us: 1.24x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.81 ms: 1.25x slower                                                   |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.4 ms: 1.30x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 270 ms: 1.30x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.76 ms: 1.30x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 64.1 ms: 1.34x slower                                                   |
| django_template                  | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                   |
| nbody                            | 42.5 ms                                                        | 59.6 ms: 1.40x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 583 us: 1.41x slower                                                    |
| generators                       | 15.7 ms                                                        | 23.4 ms: 1.49x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 66.6 ms: 1.56x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 162 ms: 1.58x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 113 ms: 3.91x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (4): async_tree_none, json, async_tree_cpu_io_mixed, async_tree_memoization
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261009-3.16.0a0-0ec3aee-NOGIL/bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.019x slower

# HPT report

- Reliability score: 93.80% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.25x