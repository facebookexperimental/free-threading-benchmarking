# Results vs. 3.13.0rc2

- fork: python
- ref: 98d462cf4de82d4ef40b
- machine: darwin-arm64
- commit hash: 98d462c
- commit date: 2025-07-29
- overall geometric mean: 1.005x faster
- HPT reliability: 76.77%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 999 ms: 1.05x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 201 ms: 2.59x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.54x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.03x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.9 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.7 ms: 1.13x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.8 ms: 2.69x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                                   |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 59.5 ms: 1.40x slower                                                   |
| Geometric mean | (ref)                                                          | 1.08x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.8 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.3 ms: 1.20x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.8 ms: 1.04x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.53 ms: 1.03x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 984 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.63 ms: 1.12x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.99 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.1 ms: 1.13x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.7 ms: 1.18x slower                                                   |
| mako            | 4.41 ms                                                        | 5.65 ms: 1.28x slower                                                   |
| django_template | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.23x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 769 us: 2.65x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 201 ms: 2.59x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.54x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 484 us: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.03x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| mdp                              | 1.06 sec                                                       | 601 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.9 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| deepcopy                         | 145 us                                                         | 119 us: 1.22x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.3 ms: 1.20x faster                                                   |
| go                               | 72.6 ms                                                        | 60.9 ms: 1.19x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 13.9 us: 1.18x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 815 ns: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.8 ms: 1.15x faster                                                   |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| float                            | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.05x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.23 us: 1.05x faster                                                   |
| docutils                         | 1.05 sec                                                       | 999 ms: 1.05x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.8 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.53 ms: 1.03x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 984 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 474 ms: 1.01x slower                                                    |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| connected_components             | 208 ms                                                         | 220 ms: 1.06x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.24 ms: 1.06x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.4 ms: 1.06x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 343 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.06 ms: 1.07x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 703 ms: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.7 ms: 1.08x slower                                                   |
| thrift                           | 309 us                                                         | 335 us: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.3 ns: 1.09x slower                                                   |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.13 ms: 1.10x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.8 ms: 1.10x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.63 ms: 1.12x slower                                                   |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 24.1 ms: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.13x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 48.7 ms: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.2 us: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.9 ms: 1.13x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 141 ms: 1.14x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.1 ms: 1.15x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.57 us: 1.15x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 43.2 ms: 1.16x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.85 us: 1.16x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.17x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 56.1 ms: 1.17x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.99 ms: 1.17x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.5 ms: 1.18x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.7 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.2 ms: 1.20x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.3 ms: 1.21x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.27 us: 1.21x slower                                                   |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.2 ms: 1.23x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.1 ms: 1.25x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.5 ms: 1.27x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.65 ms: 1.28x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 55.9 ms: 1.31x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.33 ms: 1.31x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| nbody                            | 42.5 ms                                                        | 59.5 ms: 1.40x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 600 us: 1.46x slower                                                    |
| many_optionals                   | 200 us                                                         | 328 us: 1.64x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.8 ms: 2.69x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.1 ms: 2.88x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250729-3.15.0a0-98d462c-NOGIL/bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 76.77% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x