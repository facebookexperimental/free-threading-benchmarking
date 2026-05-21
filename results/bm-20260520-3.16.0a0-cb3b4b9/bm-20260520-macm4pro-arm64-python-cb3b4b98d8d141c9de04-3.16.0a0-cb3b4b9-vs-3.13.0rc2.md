# Results vs. 3.13.0rc2

- fork: python
- ref: cb3b4b98d8d141c9de04
- machine: darwin-arm64
- commit hash: cb3b4b9
- commit date: 2026-05-20
- overall geometric mean: 1.035x faster
- HPT reliability: 98.13%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 973 ms: 1.08x faster                                                    |
| html5lib       | 23.1 ms                                                        | 22.7 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 310 ms: 1.69x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 337 ms: 1.54x faster                                                    |
| async_generators                 | 193 ms                                                         | 147 ms: 1.32x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 312 ms: 1.24x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 331 ms: 1.23x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 120 ms: 1.19x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.7 ms: 1.06x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 278 ms: 1.06x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 126 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 288 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 260 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 152 ms: 1.48x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.55x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.4 ms: 1.04x faster                                                   |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 45.1 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.73 ms: 1.10x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 47.2 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.77 ms: 1.23x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 831 ms: 1.20x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.4 ms: 1.06x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 103 us: 1.03x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.3 ms: 1.04x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 66.8 ms: 1.07x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.83 ms: 1.09x slower                                                   |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 519 ms: 2.04x faster                                                    |
| pylint                           | 106 ms                                                         | 57.0 ms: 1.85x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 310 ms: 1.69x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 337 ms: 1.54x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.18 ms: 1.50x faster                                                   |
| deepcopy                         | 145 us                                                         | 99.9 us: 1.45x faster                                                   |
| k_core                           | 1.46 sec                                                       | 1.02 sec: 1.43x faster                                                  |
| go                               | 72.6 ms                                                        | 54.1 ms: 1.34x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.32x faster                                                   |
| async_generators                 | 193 ms                                                         | 147 ms: 1.32x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 49.8 us: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 50.3 ms: 1.27x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 312 ms: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.77 ms: 1.23x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 331 ms: 1.23x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 831 ms: 1.20x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 120 ms: 1.19x faster                                                    |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.12 us: 1.15x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 876 us: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.73 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.08x faster                                                  |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                    |
| docutils                         | 1.05 sec                                                       | 973 ms: 1.08x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.4 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.7 ms: 1.06x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.89 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 278 ms: 1.06x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 126 ms: 1.06x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 1.94 ms: 1.05x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 288 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.05x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 119 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| float                            | 31.4 ms                                                        | 30.4 ms: 1.04x faster                                                   |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.5 ms: 1.03x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 314 ms: 1.03x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.3 ms: 1.02x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 22.7 ms: 1.02x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 639 ms: 1.02x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 47.2 ms: 1.01x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.81 ms: 1.01x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.4 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.0 ms: 1.01x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.59 ms: 1.01x slower                                                   |
| shortest_path                    | 225 ms                                                         | 227 ms: 1.01x slower                                                    |
| connected_components             | 208 ms                                                         | 211 ms: 1.02x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.50 us: 1.02x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 103 us: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.31 us: 1.04x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.6 ms: 1.04x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.3 ms: 1.04x slower                                                   |
| thrift                           | 309 us                                                         | 321 us: 1.04x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.51 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 489 ms: 1.04x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.3 ms: 1.04x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.5 ns: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 434 us: 1.05x slower                                                    |
| nbody                            | 42.5 ms                                                        | 45.1 ms: 1.06x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 66.8 ms: 1.07x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.30 us: 1.07x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.4 ms: 1.08x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 172 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.92 ms: 1.08x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.83 ms: 1.09x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 50.5 ms: 1.18x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 40.4 ms: 1.20x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                   |
| many_optionals                   | 200 us                                                         | 245 us: 1.22x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.7 ms: 1.24x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 260 ms: 1.25x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.8 ms: 1.26x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 152 ms: 1.48x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 58.5 ms: 1.57x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.55x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (3): regex_dna, sqlite_synth, sphinx
Ignored benchmarks (17) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, asyncio_websockets, chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260520-3.16.0a0-cb3b4b9/bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.035x faster

# HPT report

- Reliability score: 98.13% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.17x