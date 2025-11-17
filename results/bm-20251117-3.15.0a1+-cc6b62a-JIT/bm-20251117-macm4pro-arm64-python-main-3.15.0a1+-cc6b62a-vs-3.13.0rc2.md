# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: cc6b62a
- commit date: 2025-11-17
- overall geometric mean: 1.049x faster
- HPT reliability: 99.74%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.00x slower                                     |
| html5lib       | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 220 ms: 2.39x faster                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.35x faster                                     |
| async_tree_io_tg                 | 405 ms                                                         | 222 ms: 1.82x faster                                     |
| async_tree_io                    | 386 ms                                                         | 224 ms: 1.72x faster                                     |
| async_tree_none                  | 142 ms                                                         | 99.1 ms: 1.44x faster                                    |
| async_tree_none_tg               | 133 ms                                                         | 95.5 ms: 1.39x faster                                    |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.37x faster                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.35x faster                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.20x faster                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                     |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 123 ms: 1.20x slower                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.4 ms: 2.78x slower                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                    |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                     |
| nbody          | 42.5 ms                                                        | 53.9 ms: 1.27x slower                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                    |
| regex_v8       | 10.7 ms                                                        | 9.67 ms: 1.11x faster                                    |
| regex_compile  | 47.9 ms                                                        | 44.5 ms: 1.08x faster                                    |
| Geometric mean | (ref)                                                          | 1.08x faster                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a |
|----------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 810 ms: 1.23x faster                                     |
| json_dumps           | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.2 ms: 1.18x faster                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.4 ms: 1.08x faster                                    |
| unpickle_pure_python | 99.5 us                                                        | 92.4 us: 1.08x faster                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.0 ms: 1.05x faster                                    |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.03x faster                                    |
| xml_etree_parse      | 62.4 ms                                                        | 62.0 ms: 1.01x faster                                    |
| pickle_pure_python   | 130 us                                                         | 130 us: 1.00x faster                                     |
| Geometric mean       | (ref)                                                          | 1.10x faster                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a |
|------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.77 ms: 1.02x slower                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.33 ms: 1.06x slower                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a |
|-----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.35 ms: 1.01x faster                                    |
| genshi_text     | 9.97 ms                                                        | 10.3 ms: 1.03x slower                                    |
| genshi_xml      | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                    |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                    |
| Geometric mean  | (ref)                                                          | 1.07x slower                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 220 ms: 2.39x faster                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.35x faster                                     |
| async_tree_io_tg                 | 405 ms                                                         | 222 ms: 1.82x faster                                     |
| mdp                              | 1.06 sec                                                       | 609 ms: 1.74x faster                                     |
| async_tree_io                    | 386 ms                                                         | 224 ms: 1.72x faster                                     |
| richards                         | 22.1 ms                                                        | 14.2 ms: 1.55x faster                                    |
| richards_super                   | 24.7 ms                                                        | 16.3 ms: 1.52x faster                                    |
| deepcopy_memo                    | 16.5 us                                                        | 10.9 us: 1.51x faster                                    |
| deepcopy                         | 145 us                                                         | 100.0 us: 1.45x faster                                   |
| async_tree_none                  | 142 ms                                                         | 99.1 ms: 1.44x faster                                    |
| async_tree_none_tg               | 133 ms                                                         | 95.5 ms: 1.39x faster                                    |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.37x faster                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.35x faster                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.0 ms: 1.28x faster                                    |
| go                               | 72.6 ms                                                        | 57.1 ms: 1.27x faster                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                    |
| tomli_loads                      | 1000 ms                                                        | 810 ms: 1.23x faster                                     |
| json_dumps                       | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.20x faster                                     |
| pyflate                          | 222 ms                                                         | 187 ms: 1.19x faster                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.2 ms: 1.18x faster                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                    |
| pprint_safe_repr                 | 322 ms                                                         | 287 ms: 1.12x faster                                     |
| pprint_pformat                   | 650 ms                                                         | 582 ms: 1.12x faster                                     |
| telco                            | 3.07 ms                                                        | 2.76 ms: 1.11x faster                                    |
| regex_v8                         | 10.7 ms                                                        | 9.67 ms: 1.11x faster                                    |
| create_gc_cycles                 | 993 us                                                         | 908 us: 1.09x faster                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                    |
| xml_etree_process                | 25.4 ms                                                        | 23.4 ms: 1.08x faster                                    |
| float                            | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                    |
| regex_compile                    | 47.9 ms                                                        | 44.5 ms: 1.08x faster                                    |
| unpickle_pure_python             | 99.5 us                                                        | 92.4 us: 1.08x faster                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.0 ms: 1.05x faster                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.03 sec: 1.05x faster                                   |
| html5lib                         | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.1 ms: 1.04x faster                                    |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                    |
| logging_simple                   | 2.24 us                                                        | 2.16 us: 1.03x faster                                    |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                    |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                     |
| thrift                           | 309 us                                                         | 301 us: 1.03x faster                                     |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.03x faster                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                     |
| logging_format                   | 2.45 us                                                        | 2.39 us: 1.02x faster                                    |
| fannkuch                         | 179 ms                                                         | 176 ms: 1.02x faster                                     |
| mako                             | 4.41 ms                                                        | 4.35 ms: 1.01x faster                                    |
| pycparser                        | 470 ms                                                         | 466 ms: 1.01x faster                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 62.0 ms: 1.01x faster                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.03 ms: 1.01x faster                                    |
| meteor_contest                   | 47.9 ms                                                        | 47.7 ms: 1.00x faster                                    |
| pickle_pure_python               | 130 us                                                         | 130 us: 1.00x faster                                     |
| 2to3                             | 112 ms                                                         | 112 ms: 1.00x slower                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 65.5 us: 1.01x slower                                    |
| python_startup                   | 8.63 ms                                                        | 8.77 ms: 1.02x slower                                    |
| genshi_text                      | 9.97 ms                                                        | 10.3 ms: 1.03x slower                                    |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.03x slower                                    |
| dask                             | 525 ms                                                         | 545 ms: 1.04x slower                                     |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.05x slower                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.33 ms: 1.06x slower                                    |
| comprehensions                   | 6.80 us                                                        | 7.23 us: 1.06x slower                                    |
| coverage                         | 31.2 ms                                                        | 33.4 ms: 1.07x slower                                    |
| chaos                            | 24.3 ms                                                        | 26.5 ms: 1.09x slower                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                    |
| spectral_norm                    | 43.7 ms                                                        | 48.2 ms: 1.10x slower                                    |
| raytrace                         | 109 ms                                                         | 120 ms: 1.10x slower                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.1 ms: 1.10x slower                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.36 ms: 1.11x slower                                    |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                    |
| sympy_expand                     | 159 ms                                                         | 179 ms: 1.12x slower                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.02 ms: 1.14x slower                                    |
| nqueens                          | 37.2 ms                                                        | 42.6 ms: 1.14x slower                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.0 ms: 1.15x slower                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 43.7 ms: 1.16x slower                                    |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                     |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                    |
| scimark_lu                       | 42.8 ms                                                        | 50.3 ms: 1.18x slower                                    |
| pylint                           | 106 ms                                                         | 124 ms: 1.18x slower                                     |
| logging_silent                   | 40.6 ns                                                        | 48.4 ns: 1.19x slower                                    |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 123 ms: 1.20x slower                                     |
| nbody                            | 42.5 ms                                                        | 53.9 ms: 1.27x slower                                    |
| many_optionals                   | 200 us                                                         | 361 us: 1.80x slower                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.4 ms: 2.78x slower                                    |
| subparsers                       | 6.26 ms                                                        | 17.7 ms: 2.83x slower                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                             |

Benchmark hidden because not significant (3): sphinx, regex_dna, sqlite_synth
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251117-3.15.0a1+-cc6b62a-JIT/bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.049x faster

# HPT report

- Reliability score: 99.74% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.20x