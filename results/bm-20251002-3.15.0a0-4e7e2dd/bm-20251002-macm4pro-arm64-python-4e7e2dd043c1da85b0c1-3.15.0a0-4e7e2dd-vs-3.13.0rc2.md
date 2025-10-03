# Results vs. 3.13.0rc2

- fork: python
- ref: 4e7e2dd043c1da85b0c1
- machine: darwin-arm64
- commit hash: 4e7e2dd
- commit date: 2025-10-02
- overall geometric mean: 1.005x faster
- HPT reliability: 61.39%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| html5lib       | 23.1 ms                                                        | 24.7 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 253 ms: 2.08x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 258 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 256 ms: 1.59x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 257 ms: 1.50x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.7 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.0 ms: 3.08x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| float          | 31.4 ms                                                        | 31.9 ms: 1.02x slower                                                   |
| nbody          | 42.5 ms                                                        | 50.6 ms: 1.19x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.95 ms: 1.08x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 98.5 ms: 1.04x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 50.9 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.9 ms: 1.07x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 962 ms: 1.04x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.7 ms: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.9 ms: 1.02x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 104 us: 1.04x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.69 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.4 ms: 1.04x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 22.8 ms: 1.07x slower                                                   |
| mako            | 4.41 ms                                                        | 5.13 ms: 1.16x slower                                                   |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 253 ms: 2.08x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 258 ms: 2.02x faster                                                    |
| mdp                              | 1.06 sec                                                       | 552 ms: 1.92x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 256 ms: 1.59x faster                                                    |
| k_core                           | 1.46 sec                                                       | 960 ms: 1.52x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 257 ms: 1.50x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.31x faster                                                   |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| go                               | 72.6 ms                                                        | 58.8 ms: 1.23x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 54.2 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.12x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| pyflate                          | 222 ms                                                         | 204 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.08x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 919 us: 1.08x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.95 ms: 1.08x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.9 ms: 1.07x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                  |
| telco                            | 3.07 ms                                                        | 2.90 ms: 1.06x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 962 ms: 1.04x faster                                                    |
| connected_components             | 208 ms                                                         | 201 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.7 ms: 1.01x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.7 ms: 1.01x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 43.4 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.69 ms: 1.01x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 65.1 us: 1.01x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                   |
| richards                         | 22.1 ms                                                        | 22.3 ms: 1.01x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 25.0 ms: 1.01x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 962 ns: 1.02x slower                                                    |
| float                            | 31.4 ms                                                        | 31.9 ms: 1.02x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.9 ms: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 2.94 ms: 1.03x slower                                                   |
| thrift                           | 309 us                                                         | 320 us: 1.03x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 31.0 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 427 us: 1.04x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.4 ms: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 98.5 ms: 1.04x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 104 us: 1.04x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.04x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 682 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 339 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.9 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.90 ms: 1.07x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 22.8 ms: 1.07x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.7 ms: 1.07x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 51.4 ms: 1.07x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 40.0 ms: 1.07x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.63 us: 1.07x slower                                                   |
| pycparser                        | 470 ms                                                         | 505 ms: 1.08x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 171 ms: 1.08x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.3 ms: 1.08x slower                                                   |
| fannkuch                         | 179 ms                                                         | 192 ms: 1.08x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.56 ms: 1.08x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.41 us: 1.08x slower                                                   |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.0 ns: 1.08x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.7 ms: 1.10x slower                                                   |
| raytrace                         | 109 ms                                                         | 121 ms: 1.11x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 42.0 ms: 1.11x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.7 ms: 1.12x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.76 us: 1.14x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.13 ms: 1.16x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 50.2 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| nbody                            | 42.5 ms                                                        | 50.6 ms: 1.19x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| many_optionals                   | 200 us                                                         | 330 us: 1.65x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.3 ms: 2.92x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.0 ms: 3.08x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (5): json, sympy_integrate, docutils, json_loads, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251002-3.15.0a0-4e7e2dd/bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 61.39% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x