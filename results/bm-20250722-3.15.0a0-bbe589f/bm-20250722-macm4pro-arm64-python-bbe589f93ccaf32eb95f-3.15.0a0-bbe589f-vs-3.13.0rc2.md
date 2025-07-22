# Results vs. 3.13.0rc2

- fork: python
- ref: bbe589f93ccaf32eb95f
- machine: darwin-arm64
- commit hash: bbe589f
- commit date: 2025-07-22
- overall geometric mean: 1.013x faster
- HPT reliability: 64.89%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.02x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                   |
| sphinx         | 409 ms                                                         | 416 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.13x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.52x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.7 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.9 ms: 3.04x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.6 ms: 1.03x faster                                                   |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 48.7 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 97.8 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 941 ms: 1.06x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.49 ms: 1.04x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.9 ms: 1.03x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.01x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.78 ms: 1.02x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.28 ms: 1.06x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                   |
| mako            | 4.41 ms                                                        | 4.85 ms: 1.10x slower                                                   |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.13x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| mdp                              | 1.06 sec                                                       | 545 ms: 1.94x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| k_core                           | 1.46 sec                                                       | 958 ms: 1.53x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.52x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.30x faster                                                   |
| deepcopy                         | 145 us                                                         | 112 us: 1.30x faster                                                    |
| go                               | 72.6 ms                                                        | 56.5 ms: 1.28x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.7 ms: 1.26x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 199 ms: 1.12x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                   |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 941 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 956 us: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.7 ms: 1.04x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.49 ms: 1.04x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.3 ms: 1.03x faster                                                   |
| connected_components             | 208 ms                                                         | 201 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.03x faster                                                    |
| float                            | 31.4 ms                                                        | 30.6 ms: 1.03x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.9 ms: 1.03x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.1 ms: 1.02x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 63.8 us: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.82 ms: 1.01x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 40.3 ns: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 323 ms: 1.00x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.1 ms: 1.01x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.09 ms: 1.01x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 956 ns: 1.01x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 657 ms: 1.01x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.01x slower                                                    |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 44.5 ms: 1.02x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.02x slower                                                  |
| python_startup                   | 8.63 ms                                                        | 8.78 ms: 1.02x slower                                                   |
| sphinx                           | 409 ms                                                         | 416 ms: 1.02x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.3 ms: 1.02x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| fannkuch                         | 179 ms                                                         | 184 ms: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.10 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.8 ms: 1.03x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.6 ms: 1.04x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.6 ms: 1.05x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.05x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.58 us: 1.05x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.28 ms: 1.06x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 436 us: 1.06x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 50.8 ms: 1.06x slower                                                   |
| pycparser                        | 470 ms                                                         | 501 ms: 1.07x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.93 ms: 1.09x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.4 ms: 1.09x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 135 ms: 1.09x slower                                                    |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 57.1 ms: 1.09x slower                                                   |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.85 ms: 1.10x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.54 us: 1.11x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.12x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.0 ms: 1.13x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.7 ms: 1.15x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.0 ms: 1.15x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 49.8 ms: 1.16x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.2 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.24x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| many_optionals                   | 200 us                                                         | 321 us: 1.60x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.4 ms: 2.78x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.9 ms: 3.04x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (6): json, xml_etree_parse, thrift, xml_etree_process, genshi_text, sympy_integrate
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250722-3.15.0a0-bbe589f/bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.013x faster

# HPT report

- Reliability score: 64.89% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x