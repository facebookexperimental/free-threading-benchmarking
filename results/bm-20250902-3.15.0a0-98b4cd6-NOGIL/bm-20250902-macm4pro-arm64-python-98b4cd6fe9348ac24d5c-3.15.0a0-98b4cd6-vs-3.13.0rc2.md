# Results vs. 3.13.0rc2

- fork: python
- ref: 98b4cd6fe9348ac24d5c
- machine: darwin-arm64
- commit hash: 98b4cd6
- commit date: 2025-09-02
- overall geometric mean: 1.003x slower
- HPT reliability: 83.46%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| sphinx         | 409 ms                                                         | 416 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 198 ms: 2.63x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.54x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 201 ms: 2.02x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 212 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 88.3 ms: 1.50x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.40x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 11.0 ms: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.5 ms: 1.15x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.1 ms: 2.73x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 166 ms: 1.00x slower                                                    |
| nbody          | 42.5 ms                                                        | 58.0 ms: 1.36x slower                                                   |
| Geometric mean | (ref)                                                          | 1.09x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.36 ms: 1.14x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.5 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.6 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.6 ms: 1.19x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.06 ms: 1.15x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.1 ms: 1.04x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 975 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.4 ms: 1.08x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 157 us: 1.21x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.67 ms: 1.12x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.02 ms: 1.18x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.5 ms: 1.15x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.8 ms: 1.19x slower                                                   |
| django_template | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| mako            | 4.41 ms                                                        | 5.90 ms: 1.34x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.25x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 198 ms: 2.63x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 779 us: 2.62x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.54x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 479 us: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 201 ms: 2.02x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 212 ms: 1.82x faster                                                    |
| mdp                              | 1.06 sec                                                       | 602 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 88.3 ms: 1.50x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.48x faster                                                    |
| k_core                           | 1.46 sec                                                       | 997 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.40x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.6 ms: 1.19x faster                                                   |
| deepcopy                         | 145 us                                                         | 122 us: 1.18x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 14.3 us: 1.15x faster                                                   |
| go                               | 72.6 ms                                                        | 63.1 ms: 1.15x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.7 ms: 1.15x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.06 ms: 1.15x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 828 ns: 1.14x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.36 ms: 1.14x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| pyflate                          | 222 ms                                                         | 203 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                  |
| float                            | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.05x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 60.1 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 975 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.00x faster                                                   |
| pidigits                         | 166 ms                                                         | 166 ms: 1.00x slower                                                    |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                    |
| pycparser                        | 470 ms                                                         | 474 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 416 ms: 1.02x slower                                                    |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.02x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 11.0 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.5 ms: 1.03x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                   |
| fannkuch                         | 179 ms                                                         | 186 ms: 1.04x slower                                                    |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                   |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.4 ms: 1.08x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.13 ms: 1.08x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 348 ms: 1.08x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 708 ms: 1.09x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.1 ms: 1.09x slower                                                   |
| thrift                           | 309 us                                                         | 338 us: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.3 ms: 1.11x slower                                                   |
| 2to3                             | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.17 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.6 ms: 1.12x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 45.5 ns: 1.12x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.67 ms: 1.12x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 43.1 ms: 1.14x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.55 us: 1.14x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.2 ms: 1.15x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.5 ms: 1.15x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.5 ms: 1.15x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.67 ms: 1.15x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 143 ms: 1.15x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.84 us: 1.16x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 43.3 ms: 1.16x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.4 ms: 1.17x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 75.9 us: 1.17x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.6 ms: 1.18x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.02 ms: 1.18x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 113 ms: 1.19x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.8 ms: 1.19x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.9 ms: 1.19x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 157 us: 1.21x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 193 ms: 1.21x slower                                                    |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.2 ms: 1.22x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.8 ms: 1.23x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.39 us: 1.23x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.22 ms: 1.25x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.8 ms: 1.27x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.7 ms: 1.30x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.90 ms: 1.34x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 57.8 ms: 1.35x slower                                                   |
| nbody                            | 42.5 ms                                                        | 58.0 ms: 1.36x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 592 us: 1.44x slower                                                    |
| many_optionals                   | 200 us                                                         | 336 us: 1.67x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.1 ms: 2.73x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.5 ms: 2.96x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (2): async_tree_eager_cpu_io_mixed, deepcopy_reduce
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 83.46% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x