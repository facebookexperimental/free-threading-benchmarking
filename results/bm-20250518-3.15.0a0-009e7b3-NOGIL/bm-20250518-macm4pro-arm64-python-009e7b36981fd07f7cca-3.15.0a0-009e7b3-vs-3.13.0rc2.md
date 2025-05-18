# Results vs. 3.13.0rc2

- fork: python
- ref: 009e7b36981fd07f7cca
- machine: darwin-arm64
- commit hash: 009e7b3
- commit date: 2025-05-18
- overall geometric mean: 1.001x faster
- HPT reliability: 80.35%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| html5lib       | 23.1 ms                                                        | 26.2 ms: 1.13x slower                                                   |
| sphinx         | 409 ms                                                         | 419 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 88.0 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 114 ms: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 50.8 ms: 1.18x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.3 ms: 2.74x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                   |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 57.2 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.32 ms: 1.15x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 99.0 ms: 1.05x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.7 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.2 ms: 1.17x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.6 ms: 1.05x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 992 ms: 1.01x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.83 ms: 1.04x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.6 ms: 1.09x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| json_loads           | 10.8 us                                                        | 12.8 us: 1.18x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 156 us: 1.20x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.45 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.88 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.5 ms: 1.16x slower                                                   |
| mako            | 4.41 ms                                                        | 5.71 ms: 1.29x slower                                                   |
| django_template | 12.5 ms                                                        | 17.2 ms: 1.38x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.23x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.66x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 777 us: 2.63x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 484 us: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                    |
| mdp                              | 1.06 sec                                                       | 580 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 88.0 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 997 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.2 ms: 1.17x faster                                                   |
| deepcopy                         | 145 us                                                         | 126 us: 1.15x faster                                                    |
| go                               | 72.6 ms                                                        | 63.1 ms: 1.15x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.6 ms: 1.15x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 824 ns: 1.15x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 14.3 us: 1.15x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.32 ms: 1.15x faster                                                   |
| pyflate                          | 222 ms                                                         | 199 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                   |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 59.6 ms: 1.05x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 992 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 476 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 419 ms: 1.03x slower                                                    |
| shortest_path                    | 225 ms                                                         | 231 ms: 1.03x slower                                                    |
| fannkuch                         | 179 ms                                                         | 185 ms: 1.04x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.83 ms: 1.04x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 99.0 ms: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 219 ms: 1.05x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.06 ms: 1.07x slower                                                   |
| json                             | 1.94 ms                                                        | 2.10 ms: 1.08x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 27.6 ms: 1.09x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                    |
| thrift                           | 309 us                                                         | 337 us: 1.09x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.45 ms: 1.09x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.37 ms: 1.10x slower                                                   |
| richards                         | 22.1 ms                                                        | 24.2 ms: 1.10x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.10x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 114 ms: 1.11x slower                                                    |
| 2to3                             | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 359 ms: 1.12x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.6 ms: 1.12x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.12x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.7 ms: 1.12x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 730 ms: 1.12x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.8 ms: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.7 ms: 1.13x slower                                                   |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 26.2 ms: 1.13x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.5 ms: 1.16x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.88 ms: 1.16x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 55.5 ms: 1.16x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 144 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.1 ms: 1.17x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 76.0 us: 1.18x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 50.8 ms: 1.18x slower                                                   |
| json_loads                       | 10.8 us                                                        | 12.8 us: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.9 ms: 1.19x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 52.3 ms: 1.20x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 156 us: 1.20x slower                                                    |
| raytrace                         | 109 ms                                                         | 132 ms: 1.22x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.6 ms: 1.22x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.18 ms: 1.23x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.9 ms: 1.28x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.86 us: 1.28x slower                                                   |
| many_optionals                   | 200 us                                                         | 258 us: 1.29x slower                                                    |
| logging_format                   | 2.45 us                                                        | 3.16 us: 1.29x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.3 ms: 1.29x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.71 ms: 1.29x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.84 us: 1.30x slower                                                   |
| nbody                            | 42.5 ms                                                        | 57.2 ms: 1.34x slower                                                   |
| django_template                  | 12.5 ms                                                        | 17.2 ms: 1.38x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 601 us: 1.46x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 65.6 ms: 1.53x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 9.93 ms: 1.59x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.3 ms: 2.74x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 217 ns: 5.34x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (2): deepcopy_reduce, pathlib
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250518-3.15.0a0-009e7b3-NOGIL/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 80.35% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x