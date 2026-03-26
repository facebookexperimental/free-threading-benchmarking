# Results vs. 3.13.0rc2

- fork: python
- ref: 8e1469c952fb9db57efd
- machine: darwin-arm64
- commit hash: 8e1469c
- commit date: 2026-03-26
- overall geometric mean: 1.080x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.02x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.1 ms: 1.10x faster                                                    |
| sphinx         | 409 ms                                                         | 396 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 221 ms: 2.37x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 231 ms: 1.75x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 229 ms: 1.69x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.6 ms: 1.43x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 96.7 ms: 1.37x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.35x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 249 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.9 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.5 ms: 2.82x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.7 ms: 1.18x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.3 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.79 ms: 1.09x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.4 ms: 1.03x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.3 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|---------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps          | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                    |
| tomli_loads         | 1000 ms                                                        | 827 ms: 1.21x faster                                                     |
| xml_etree_iterparse | 46.1 ms                                                        | 40.3 ms: 1.14x faster                                                    |
| xml_etree_process   | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                    |
| xml_etree_generate  | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                    |
| json_loads          | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| xml_etree_parse     | 62.4 ms                                                        | 64.1 ms: 1.03x slower                                                    |
| pickle_pure_python  | 130 us                                                         | 139 us: 1.07x slower                                                     |
| Geometric mean      | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.28 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.78 ms: 1.02x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 221 ms: 2.37x faster                                                     |
| mdp                              | 1.06 sec                                                       | 539 ms: 1.96x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 231 ms: 1.75x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 229 ms: 1.69x faster                                                     |
| k_core                           | 1.46 sec                                                       | 898 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.97 ms: 1.58x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.5 us: 1.47x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.6 ms: 1.43x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.42x faster                                                    |
| go                               | 72.6 ms                                                        | 52.5 ms: 1.38x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 96.7 ms: 1.37x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.35x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.35x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.2 ms: 1.30x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 827 ms: 1.21x faster                                                     |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 249 ms: 1.18x faster                                                     |
| float                            | 31.4 ms                                                        | 26.7 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.3 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.11x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 899 us: 1.11x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 21.1 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.79 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.9 ms: 1.08x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.5 ms: 1.07x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.07x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.88 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 168 ms: 1.06x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 23.2 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 41.7 ms: 1.05x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 311 ms: 1.04x faster                                                     |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                    |
| sphinx                           | 409 ms                                                         | 396 ms: 1.03x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.16 us: 1.03x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.4 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.38 us: 1.03x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 632 ms: 1.03x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.78 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nqueens                          | 37.2 ms                                                        | 36.6 ms: 1.02x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 63.8 us: 1.01x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 520 ms: 1.01x faster                                                     |
| deltablue                        | 1.45 ms                                                        | 1.44 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.49 ms: 1.00x faster                                                    |
| connected_components             | 208 ms                                                         | 207 ms: 1.00x faster                                                     |
| chaos                            | 24.3 ms                                                        | 24.4 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.3 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.80 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                    |
| 2to3                             | 112 ms                                                         | 113 ms: 1.02x slower                                                     |
| thrift                           | 309 us                                                         | 314 us: 1.02x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 41.4 ns: 1.02x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 64.1 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.1 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.6 ms: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 427 us: 1.04x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.07 us: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                     |
| nbody                            | 42.5 ms                                                        | 44.3 ms: 1.04x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.9 ms: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.28 ms: 1.06x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.9 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                     |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.14x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 38.8 ms: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.6 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 247 us: 1.23x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.5 ms: 2.82x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (4): pycparser, sqlite_synth, unpickle_pure_python, gc_traversal
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260326-3.15.0a7+-8e1469c/bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.080x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.19x