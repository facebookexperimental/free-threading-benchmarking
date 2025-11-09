# Results vs. 3.13.0rc2

- fork: python
- ref: 0ac890bea79d3e0162c8
- machine: darwin-arm64
- commit hash: 0ac890b
- commit date: 2025-11-08
- overall geometric mean: 1.004x faster
- HPT reliability: 67.73%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.11x slower                                                     |
| docutils       | 1.05 sec                                                       | 987 ms: 1.06x faster                                                     |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 86.7 ms: 1.53x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 49.2 ms: 1.14x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.7 ms: 2.69x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                    |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.8 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.39 ms: 1.14x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.4 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 53.4 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.08 ms: 1.14x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.4 ms: 1.05x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 967 ms: 1.03x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 37.6 ms: 1.05x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.12x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.18x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.59 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.98 ms: 1.17x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.4 ms: 1.14x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.8 ms: 1.18x slower                                                    |
| mako            | 4.41 ms                                                        | 5.81 ms: 1.32x slower                                                    |
| django_template | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.24x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 758 us: 2.69x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 470 us: 2.11x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                     |
| mdp                              | 1.06 sec                                                       | 606 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 86.7 ms: 1.53x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                     |
| k_core                           | 1.46 sec                                                       | 989 ms: 1.48x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.3 us: 1.24x faster                                                    |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| go                               | 72.6 ms                                                        | 61.9 ms: 1.17x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.4 ms: 1.16x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.08 ms: 1.14x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.39 ms: 1.14x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 837 ns: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                     |
| docutils                         | 1.05 sec                                                       | 987 ms: 1.06x faster                                                     |
| float                            | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.02 sec: 1.05x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 59.4 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 967 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.27 us: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.4 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                     |
| fannkuch                         | 179 ms                                                         | 183 ms: 1.03x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.03x slower                                                    |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                    |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.6 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.05 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 135 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                     |
| richards                         | 22.1 ms                                                        | 24.1 ms: 1.09x slower                                                    |
| thrift                           | 309 us                                                         | 338 us: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 44.9 ns: 1.10x slower                                                    |
| 2to3                             | 112 ms                                                         | 123 ms: 1.11x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.11x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.59 ms: 1.11x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 53.4 ms: 1.11x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.5 ms: 1.11x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 358 ms: 1.11x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.12x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.53 us: 1.13x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 737 ms: 1.13x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 49.2 ms: 1.14x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 24.4 ms: 1.14x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.3 ms: 1.15x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 43.5 ms: 1.15x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.83 us: 1.16x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 74.7 us: 1.16x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.6 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.5 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 51.3 ms: 1.17x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.98 ms: 1.17x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.18x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.8 ms: 1.18x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 44.3 ms: 1.19x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                                     |
| chaos                            | 24.3 ms                                                        | 29.2 ms: 1.20x slower                                                    |
| raytrace                         | 109 ms                                                         | 132 ms: 1.21x slower                                                     |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.22x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.56 us: 1.26x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.26 ms: 1.27x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.9 ms: 1.28x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.1 ms: 1.28x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 535 us: 1.30x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 56.0 ms: 1.31x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.81 ms: 1.32x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.8 ms: 1.34x slower                                                    |
| many_optionals                   | 200 us                                                         | 379 us: 1.89x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.7 ms: 2.69x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 19.1 ms: 3.05x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (4): pycparser, async_tree_eager_cpu_io_mixed, telco, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251108-3.15.0a1+-0ac890b-NOGIL/bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 67.73% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x