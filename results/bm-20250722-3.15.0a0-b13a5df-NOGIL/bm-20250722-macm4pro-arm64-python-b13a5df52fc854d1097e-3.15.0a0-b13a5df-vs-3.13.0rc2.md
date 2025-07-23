# Results vs. 3.13.0rc2

- fork: python
- ref: b13a5df52fc854d1097e
- machine: darwin-arm64
- commit hash: b13a5df
- commit date: 2025-07-22
- overall geometric mean: 1.009x faster
- HPT reliability: 75.03%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 998 ms: 1.05x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 409 ms                                                         | 415 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.59x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.06x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 85.6 ms: 1.55x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.9 ms: 1.43x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.5 ms: 1.12x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.1 ms: 2.66x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.2 ms: 1.12x faster                                                   |
| pidigits       | 166 ms                                                         | 166 ms: 1.00x slower                                                    |
| nbody          | 42.5 ms                                                        | 55.3 ms: 1.30x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.21 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.3 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 964 ms: 1.04x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.61 ms: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.5 ms: 1.04x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.8 us: 1.09x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 150 us: 1.15x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.70 ms: 1.12x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.05 ms: 1.18x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.6 ms: 1.10x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                   |
| mako            | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                   |
| django_template | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.69x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 782 us: 2.61x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.59x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.06x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 487 us: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| mdp                              | 1.06 sec                                                       | 604 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 85.6 ms: 1.55x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 988 ms: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.9 ms: 1.43x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| deepcopy                         | 145 us                                                         | 118 us: 1.23x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.6 us: 1.21x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| go                               | 72.6 ms                                                        | 60.0 ms: 1.21x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 814 ns: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.21 ms: 1.16x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.8 ms: 1.15x faster                                                   |
| pyflate                          | 222 ms                                                         | 199 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| float                            | 31.4 ms                                                        | 28.2 ms: 1.12x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 998 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.04x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 964 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.61 ms: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 166 ms: 1.00x slower                                                    |
| pycparser                        | 470 ms                                                         | 473 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 415 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 232 ms: 1.03x slower                                                    |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.04x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.5 ms: 1.04x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.1 ms: 1.05x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.23 ms: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 219 ms: 1.06x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.4 ms: 1.07x slower                                                   |
| thrift                           | 309 us                                                         | 331 us: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.10 ms: 1.08x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.8 us: 1.09x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 350 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.3 ns: 1.09x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.3 ms: 1.09x slower                                                   |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 712 ms: 1.10x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.12 ms: 1.10x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.6 ms: 1.10x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.12x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.70 ms: 1.12x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 48.5 ms: 1.12x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 49.5 ms: 1.13x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.54 us: 1.13x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 141 ms: 1.14x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.8 us: 1.14x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.81 us: 1.15x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 150 us: 1.15x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.6 ms: 1.17x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.0 ms: 1.17x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.8 ms: 1.18x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.05 ms: 1.18x slower                                                   |
| raytrace                         | 109 ms                                                         | 129 ms: 1.19x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.1 ms: 1.20x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.5 ms: 1.20x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.26 us: 1.21x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.3 ms: 1.23x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.4 ms: 1.26x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.7 ms: 1.27x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.28 ms: 1.28x slower                                                   |
| nbody                            | 42.5 ms                                                        | 55.3 ms: 1.30x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 56.2 ms: 1.31x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 583 us: 1.42x slower                                                    |
| many_optionals                   | 200 us                                                         | 330 us: 1.65x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.1 ms: 2.66x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.2 ms: 2.91x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (1): pathlib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250722-3.15.0a0-b13a5df-NOGIL/bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.009x faster

# HPT report

- Reliability score: 75.03% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x