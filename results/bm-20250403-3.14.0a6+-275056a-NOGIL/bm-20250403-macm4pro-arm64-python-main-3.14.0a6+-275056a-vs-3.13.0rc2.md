# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 275056a
- commit date: 2025-04-03
- overall geometric mean: 1.013x faster
- HPT reliability: 70.86%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.07x slower                                     |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                   |
| html5lib       | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                    |
| sphinx         | 409 ms                                                         | 423 ms: 1.03x slower                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.65x faster                                     |
| async_tree_eager_io              | 525 ms                                                         | 209 ms: 2.52x faster                                     |
| async_tree_io_tg                 | 405 ms                                                         | 200 ms: 2.03x faster                                     |
| async_tree_io                    | 386 ms                                                         | 213 ms: 1.81x faster                                     |
| async_tree_none_tg               | 133 ms                                                         | 87.6 ms: 1.51x faster                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.49x faster                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                     |
| async_tree_memoization           | 184 ms                                                         | 132 ms: 1.40x faster                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 231 ms: 1.30x faster                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 222 ms: 1.07x slower                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                     |
| async_tree_eager                 | 43.2 ms                                                        | 51.0 ms: 1.18x slower                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.3 ms: 2.71x slower                                    |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                     |
| nbody          | 42.5 ms                                                        | 53.8 ms: 1.27x slower                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                    |
| regex_v8       | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                    |
| regex_dna      | 94.6 ms                                                        | 101 ms: 1.06x slower                                     |
| regex_compile  | 47.9 ms                                                        | 53.6 ms: 1.12x slower                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a |
|----------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.0 ms: 1.21x faster                                    |
| xml_etree_parse      | 62.4 ms                                                        | 57.5 ms: 1.09x faster                                    |
| tomli_loads          | 1000 ms                                                        | 965 ms: 1.04x faster                                     |
| xml_etree_generate   | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                    |
| unpickle_pure_python | 99.5 us                                                        | 107 us: 1.08x slower                                     |
| json_dumps           | 4.65 ms                                                        | 5.07 ms: 1.09x slower                                    |
| json_loads           | 10.8 us                                                        | 11.9 us: 1.10x slower                                    |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                     |
| Geometric mean       | (ref)                                                          | 1.02x slower                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a |
|------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.47 ms: 1.10x slower                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.52 ms: 1.26x slower                                    |
| Geometric mean         | (ref)                                                          | 1.18x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a |
|-----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                    |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                    |
| mako            | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                    |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                    |
| Geometric mean  | (ref)                                                          | 1.21x slower                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 753 us: 2.71x faster                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.65x faster                                     |
| async_tree_eager_io              | 525 ms                                                         | 209 ms: 2.52x faster                                     |
| create_gc_cycles                 | 993 us                                                         | 459 us: 2.16x faster                                     |
| async_tree_io_tg                 | 405 ms                                                         | 200 ms: 2.03x faster                                     |
| mdp                              | 1.06 sec                                                       | 571 ms: 1.85x faster                                     |
| async_tree_io                    | 386 ms                                                         | 213 ms: 1.81x faster                                     |
| async_tree_none_tg               | 133 ms                                                         | 87.6 ms: 1.51x faster                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.49x faster                                     |
| k_core                           | 1.46 sec                                                       | 990 ms: 1.48x faster                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                     |
| async_tree_memoization           | 184 ms                                                         | 132 ms: 1.40x faster                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 231 ms: 1.30x faster                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.0 ms: 1.21x faster                                    |
| deepcopy                         | 145 us                                                         | 124 us: 1.17x faster                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.9 ms: 1.17x faster                                    |
| sqlite_synth                     | 948 ns                                                         | 814 ns: 1.16x faster                                     |
| go                               | 72.6 ms                                                        | 62.8 ms: 1.15x faster                                    |
| deepcopy_memo                    | 16.5 us                                                        | 14.4 us: 1.14x faster                                    |
| float                            | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                    |
| pyflate                          | 222 ms                                                         | 201 ms: 1.10x faster                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 57.5 ms: 1.09x faster                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                    |
| regex_v8                         | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                    |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                   |
| tomli_loads                      | 1000 ms                                                        | 965 ms: 1.04x faster                                     |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                     |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.28 us: 1.01x faster                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                    |
| html5lib                         | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                    |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.02x slower                                    |
| shortest_path                    | 225 ms                                                         | 230 ms: 1.02x slower                                     |
| xml_etree_generate               | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                    |
| sphinx                           | 409 ms                                                         | 423 ms: 1.03x slower                                     |
| connected_components             | 208 ms                                                         | 218 ms: 1.05x slower                                     |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                    |
| regex_dna                        | 94.6 ms                                                        | 101 ms: 1.06x slower                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 222 ms: 1.07x slower                                     |
| 2to3                             | 112 ms                                                         | 120 ms: 1.07x slower                                     |
| unpickle_pure_python             | 99.5 us                                                        | 107 us: 1.08x slower                                     |
| fannkuch                         | 179 ms                                                         | 194 ms: 1.08x slower                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.17 ms: 1.09x slower                                    |
| json_dumps                       | 4.65 ms                                                        | 5.07 ms: 1.09x slower                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 41.4 ms: 1.10x slower                                    |
| python_startup                   | 8.63 ms                                                        | 9.47 ms: 1.10x slower                                    |
| json_loads                       | 10.8 us                                                        | 11.9 us: 1.10x slower                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                     |
| genshi_xml                       | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                    |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.11x slower                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.1 ms: 1.11x slower                                    |
| regex_compile                    | 47.9 ms                                                        | 53.6 ms: 1.12x slower                                    |
| richards                         | 22.1 ms                                                        | 24.7 ms: 1.12x slower                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 72.4 us: 1.12x slower                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                     |
| telco                            | 3.07 ms                                                        | 3.46 ms: 1.13x slower                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 50.2 ms: 1.13x slower                                    |
| pprint_safe_repr                 | 322 ms                                                         | 365 ms: 1.13x slower                                     |
| pprint_pformat                   | 650 ms                                                         | 737 ms: 1.13x slower                                     |
| richards_super                   | 24.7 ms                                                        | 28.1 ms: 1.14x slower                                    |
| nqueens                          | 37.2 ms                                                        | 42.4 ms: 1.14x slower                                    |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.74 ms: 1.15x slower                                    |
| scimark_fft                      | 124 ms                                                         | 142 ms: 1.15x slower                                     |
| logging_silent                   | 40.6 ns                                                        | 46.9 ns: 1.15x slower                                    |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                     |
| deltablue                        | 1.45 ms                                                        | 1.68 ms: 1.16x slower                                    |
| logging_format                   | 2.45 us                                                        | 2.84 us: 1.16x slower                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.6 ms: 1.16x slower                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                     |
| spectral_norm                    | 43.7 ms                                                        | 51.0 ms: 1.17x slower                                    |
| logging_simple                   | 2.24 us                                                        | 2.61 us: 1.17x slower                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.6 ms: 1.18x slower                                    |
| async_tree_eager                 | 43.2 ms                                                        | 51.0 ms: 1.18x slower                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.12 ms: 1.19x slower                                    |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                     |
| many_optionals                   | 200 us                                                         | 240 us: 1.20x slower                                     |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                    |
| chaos                            | 24.3 ms                                                        | 29.1 ms: 1.20x slower                                    |
| raytrace                         | 109 ms                                                         | 131 ms: 1.21x slower                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 41.0 ms: 1.22x slower                                    |
| coverage                         | 31.2 ms                                                        | 38.8 ms: 1.24x slower                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.52 ms: 1.26x slower                                    |
| nbody                            | 42.5 ms                                                        | 53.8 ms: 1.27x slower                                    |
| scimark_lu                       | 42.8 ms                                                        | 54.3 ms: 1.27x slower                                    |
| comprehensions                   | 6.80 us                                                        | 8.65 us: 1.27x slower                                    |
| mako                             | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                    |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                    |
| subparsers                       | 6.26 ms                                                        | 8.75 ms: 1.40x slower                                    |
| bench_thread_pool                | 412 us                                                         | 577 us: 1.40x slower                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.3 ms: 2.71x slower                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                             |

Benchmark hidden because not significant (1): pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250403-3.14.0a6+-275056a-NOGIL/bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.013x faster

# HPT report

- Reliability score: 70.86% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.18x