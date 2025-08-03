# Results vs. 3.13.0rc2

- fork: python
- ref: 801cf3fcdd27d8b6dd0f
- machine: darwin-arm64
- commit hash: 801cf3f
- commit date: 2025-08-02
- overall geometric mean: 1.017x faster
- HPT reliability: 85.58%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.05x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.13x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.52x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| async_generators                 | 193 ms                                                         | 185 ms: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.0 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.2 ms: 3.01x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 57.0 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                          | 1.10x slower                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.61 ms: 1.11x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 823 ms: 1.21x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.28 ms: 1.09x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 92.8 us: 1.07x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.0 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.3 ms: 1.04x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.91 ms: 1.01x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.13x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                    |
| mdp                              | 1.06 sec                                                       | 541 ms: 1.96x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.52x faster                                                    |
| k_core                           | 1.46 sec                                                       | 990 ms: 1.48x faster                                                    |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.0 ms: 1.28x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.28x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.0 us: 1.27x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| go                               | 72.6 ms                                                        | 57.5 ms: 1.26x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 823 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.61 ms: 1.11x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.28 ms: 1.09x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 599 ms: 1.08x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 297 ms: 1.08x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 92.8 us: 1.07x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 24.0 ms: 1.06x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 941 us: 1.06x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.92 ms: 1.05x faster                                                   |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.04x faster                                                    |
| async_generators                 | 193 ms                                                         | 185 ms: 1.04x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.3 ms: 1.04x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.0 ms: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 63.8 us: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 941 ns: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.91 ms: 1.01x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 43.5 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.86 ms: 1.01x slower                                                   |
| thrift                           | 309 us                                                         | 311 us: 1.01x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| python_startup                   | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.61 ms: 1.01x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 41.3 ns: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.02x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.09 ms: 1.02x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.4 ms: 1.03x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.9 ms: 1.03x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                   |
| connected_components             | 208 ms                                                         | 216 ms: 1.04x slower                                                    |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.9 ms: 1.05x slower                                                   |
| 2to3                             | 112 ms                                                         | 118 ms: 1.05x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.58 us: 1.06x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 438 us: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 500 ms: 1.06x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.7 ms: 1.07x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.30 us: 1.07x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.2 ms: 1.08x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.08x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 173 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                    |
| raytrace                         | 109 ms                                                         | 119 ms: 1.10x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.9 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.12x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.2 ms: 1.13x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.8 ms: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.66 ms: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.2 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.13 ms: 1.20x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.0 ms: 1.34x slower                                                   |
| many_optionals                   | 200 us                                                         | 324 us: 1.62x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.3 ms: 2.77x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.2 ms: 3.01x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (8): json, xml_etree_parse, sphinx, richards, richards_super, regex_compile, float, mako
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.017x faster

# HPT report

- Reliability score: 85.58% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x