# Results vs. 3.13.0rc2

- fork: python
- ref: bc2872445b2aee4bb4e0
- machine: darwin-arm64
- commit hash: bc28724
- commit date: 2025-08-18
- overall geometric mean: 1.002x faster
- HPT reliability: 78.97%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 993 ms: 1.05x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.9 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.0 ms: 1.14x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.0 ms: 2.70x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 57.4 ms: 1.35x slower                                                   |
| Geometric mean | (ref)                                                          | 1.08x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.26 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.3 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 3.96 ms: 1.18x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.2 ms: 1.05x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.13x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.59 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.95 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.4 ms: 1.14x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.8 ms: 1.19x slower                                                   |
| django_template | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| mako            | 4.41 ms                                                        | 5.87 ms: 1.33x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.24x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.68x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 767 us: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 483 us: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                    |
| mdp                              | 1.06 sec                                                       | 608 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.9 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 990 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.22x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                   |
| deepcopy                         | 145 us                                                         | 120 us: 1.21x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.96 ms: 1.18x faster                                                   |
| go                               | 72.6 ms                                                        | 62.0 ms: 1.17x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 14.2 us: 1.16x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.26 ms: 1.16x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 56.0 ms: 1.14x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 831 ns: 1.14x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| pyflate                          | 222 ms                                                         | 201 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 59.2 ms: 1.05x faster                                                   |
| docutils                         | 1.05 sec                                                       | 993 ms: 1.05x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.02 sec: 1.05x faster                                                  |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.26 us: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 473 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 96.3 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| fannkuch                         | 179 ms                                                         | 187 ms: 1.05x slower                                                    |
| shortest_path                    | 225 ms                                                         | 236 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                   |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                    |
| connected_components             | 208 ms                                                         | 224 ms: 1.08x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.8 ms: 1.08x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.12 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.1 ms: 1.10x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 354 ms: 1.10x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 722 ms: 1.11x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.59 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.18 ms: 1.12x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 45.5 ns: 1.12x slower                                                   |
| thrift                           | 309 us                                                         | 347 us: 1.12x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.13x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.53 us: 1.13x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.0 ms: 1.14x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.0 ms: 1.14x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.4 ms: 1.14x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.81 us: 1.15x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 142 ms: 1.15x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 74.4 us: 1.15x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.95 ms: 1.17x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.18x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 113 ms: 1.18x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.8 ms: 1.18x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 44.0 ms: 1.18x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.8 ms: 1.19x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.3 ms: 1.20x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 57.7 ms: 1.20x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 193 ms: 1.21x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.21x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 53.4 ms: 1.22x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.7 ms: 1.22x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.39 us: 1.23x slower                                                   |
| raytrace                         | 109 ms                                                         | 135 ms: 1.24x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 43.1 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.3 ms: 1.29x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.31 ms: 1.30x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.87 ms: 1.33x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 57.8 ms: 1.35x slower                                                   |
| nbody                            | 42.5 ms                                                        | 57.4 ms: 1.35x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 599 us: 1.45x slower                                                    |
| many_optionals                   | 200 us                                                         | 330 us: 1.65x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.0 ms: 2.70x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.3 ms: 2.93x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (4): sphinx, coroutines, tomli_loads, telco
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250818-3.15.0a0-bc28724-NOGIL/bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 78.97% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x