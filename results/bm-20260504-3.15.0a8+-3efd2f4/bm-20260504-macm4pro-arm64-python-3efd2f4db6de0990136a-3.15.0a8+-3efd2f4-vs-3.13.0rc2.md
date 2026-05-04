# Results vs. 3.13.0rc2

- fork: python
- ref: 3efd2f4db6de0990136a
- machine: darwin-arm64
- commit hash: 3efd2f4
- commit date: 2026-05-04
- overall geometric mean: 1.050x faster
- HPT reliability: 99.95%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 964 ms: 1.09x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 307 ms: 1.71x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 335 ms: 1.55x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 309 ms: 1.25x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 331 ms: 1.23x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 119 ms: 1.20x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.2 ms: 1.07x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 175 ms: 1.06x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 278 ms: 1.05x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 289 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 260 ms: 1.25x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 150 ms: 1.47x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 102 ms: 3.52x slower                                                     |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.6 ms: 1.06x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 45.1 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.68 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.4 ms: 1.06x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.4 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|---------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps          | 4.65 ms                                                        | 3.77 ms: 1.23x faster                                                    |
| tomli_loads         | 1000 ms                                                        | 836 ms: 1.20x faster                                                     |
| xml_etree_iterparse | 46.1 ms                                                        | 42.4 ms: 1.09x faster                                                    |
| json_loads          | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| xml_etree_generate  | 35.8 ms                                                        | 35.9 ms: 1.00x slower                                                    |
| pickle_pure_python  | 130 us                                                         | 141 us: 1.08x slower                                                     |
| xml_etree_parse     | 62.4 ms                                                        | 68.5 ms: 1.10x slower                                                    |
| Geometric mean      | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (2): xml_etree_process, unpickle_pure_python

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.70 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 540 ms: 1.96x faster                                                     |
| pylint                           | 106 ms                                                         | 56.8 ms: 1.86x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 307 ms: 1.71x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.97 ms: 1.58x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 335 ms: 1.55x faster                                                     |
| deepcopy                         | 145 us                                                         | 98.6 us: 1.47x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.45x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                    |
| go                               | 72.6 ms                                                        | 52.9 ms: 1.37x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.1 ms: 1.28x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 309 ms: 1.25x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.77 ms: 1.23x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 331 ms: 1.23x faster                                                     |
| pyflate                          | 222 ms                                                         | 182 ms: 1.22x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 119 ms: 1.20x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 836 ms: 1.20x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 877 us: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.68 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.81 ms: 1.09x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.4 ms: 1.09x faster                                                    |
| fannkuch                         | 179 ms                                                         | 164 ms: 1.09x faster                                                     |
| docutils                         | 1.05 sec                                                       | 964 ms: 1.09x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.2 ms: 1.07x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.7 ms: 1.06x faster                                                    |
| float                            | 31.4 ms                                                        | 29.6 ms: 1.06x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 45.4 ms: 1.06x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 35.3 ms: 1.06x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 175 ms: 1.06x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 278 ms: 1.05x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.3 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.5 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 289 ms: 1.04x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 624 ms: 1.04x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 310 ms: 1.04x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 1.97 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                    |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.7 us: 1.03x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 933 ns: 1.02x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 43.1 ms: 1.01x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 40.1 ns: 1.01x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.42 us: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.45 ms: 1.01x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                     |
| connected_components             | 208 ms                                                         | 207 ms: 1.00x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 35.9 ms: 1.00x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.4 ms: 1.01x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.7 ms: 1.02x slower                                                    |
| thrift                           | 309 us                                                         | 314 us: 1.02x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 6.94 us: 1.02x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.03x slower                                                    |
| pycparser                        | 470 ms                                                         | 485 ms: 1.03x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 98.7 ms: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.1 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.1 ms: 1.05x slower                                                    |
| nbody                            | 42.5 ms                                                        | 45.1 ms: 1.06x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.70 ms: 1.07x slower                                                    |
| raytrace                         | 109 ms                                                         | 116 ms: 1.07x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.91 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                     |
| coverage                         | 31.2 ms                                                        | 33.9 ms: 1.09x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 46.6 ms: 1.09x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 68.5 ms: 1.10x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.6 ms: 1.12x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 39.2 ms: 1.17x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                    |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 260 ms: 1.25x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 47.4 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 150 ms: 1.47x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 102 ms: 3.52x slower                                                     |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (3): sphinx, xml_etree_process, unpickle_pure_python
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260504-3.15.0a8+-3efd2f4/bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.050x faster

# HPT report

- Reliability score: 99.95% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.17x