# Results vs. 3.13.0rc2

- fork: python
- ref: c4bcc6a77864b42574ec
- machine: darwin-arm64
- commit hash: c4bcc6a
- commit date: 2025-05-06
- overall geometric mean: 1.013x faster
- HPT reliability: 65.57%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.08x slower                                                     |
| docutils       | 1.05 sec                                                       | 995 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 25.4 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.06x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 87.3 ms: 1.52x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.41x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 50.6 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.5 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 158 ms: 1.05x faster                                                     |
| nbody          | 42.5 ms                                                        | 55.7 ms: 1.31x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.38 ms: 1.14x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.5 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 52.5 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.1 ms: 1.21x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.2 ms: 1.05x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 978 ms: 1.02x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.6 ms: 1.05x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 107 us: 1.08x slower                                                     |
| json_dumps           | 4.65 ms                                                        | 5.18 ms: 1.11x slower                                                    |
| json_loads           | 10.8 us                                                        | 12.3 us: 1.13x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 150 us: 1.15x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.35 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.81 ms: 1.14x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| mako            | 4.41 ms                                                        | 5.57 ms: 1.26x slower                                                    |
| django_template | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 753 us: 2.71x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 467 us: 2.13x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.06x faster                                                     |
| mdp                              | 1.06 sec                                                       | 572 ms: 1.85x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 87.3 ms: 1.52x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                     |
| k_core                           | 1.46 sec                                                       | 986 ms: 1.48x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.41x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.1 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                     |
| go                               | 72.6 ms                                                        | 61.8 ms: 1.17x faster                                                    |
| deepcopy                         | 145 us                                                         | 124 us: 1.17x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 14.1 us: 1.16x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 819 ns: 1.16x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.8 ms: 1.15x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.38 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 201 ms: 1.11x faster                                                     |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.2 ms: 1.05x faster                                                    |
| docutils                         | 1.05 sec                                                       | 995 ms: 1.05x faster                                                     |
| pidigits                         | 166 ms                                                         | 158 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 978 ms: 1.02x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.27 us: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.5 ms: 1.01x slower                                                    |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                    |
| shortest_path                    | 225 ms                                                         | 232 ms: 1.03x slower                                                     |
| json                             | 1.94 ms                                                        | 2.03 ms: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.6 ms: 1.05x slower                                                    |
| connected_components             | 208 ms                                                         | 218 ms: 1.05x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.94 ms: 1.05x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.25 ms: 1.06x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 107 us: 1.08x slower                                                     |
| 2to3                             | 112 ms                                                         | 121 ms: 1.08x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.35 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.11 ms: 1.09x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.5 ms: 1.10x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.2 ms: 1.10x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 353 ms: 1.10x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 25.4 ms: 1.10x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 716 ms: 1.10x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 44.7 ns: 1.10x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.1 ms: 1.10x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 27.4 ms: 1.11x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.18 ms: 1.11x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 49.6 ms: 1.12x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.3 ms: 1.13x slower                                                    |
| json_loads                       | 10.8 us                                                        | 12.3 us: 1.13x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 42.9 ms: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.72 ms: 1.14x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.81 ms: 1.14x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.2 ms: 1.14x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 150 us: 1.15x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.5 ms: 1.16x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 75.1 us: 1.16x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 50.6 ms: 1.17x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.62 us: 1.17x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.4 ms: 1.17x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.89 us: 1.18x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.9 ms: 1.19x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.1 ms: 1.20x slower                                                    |
| raytrace                         | 109 ms                                                         | 132 ms: 1.21x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 152 ms: 1.23x slower                                                     |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 42.0 ms: 1.25x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.57 ms: 1.26x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.64 us: 1.27x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.0 ms: 1.28x slower                                                    |
| nbody                            | 42.5 ms                                                        | 55.7 ms: 1.31x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 58.6 ms: 1.37x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 583 us: 1.42x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.72 ms: 1.53x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.62 ms: 1.54x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.5 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (2): pycparser, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250506-3.14.0a7+-c4bcc6a-NOGIL/bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.013x faster

# HPT report

- Reliability score: 65.57% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x