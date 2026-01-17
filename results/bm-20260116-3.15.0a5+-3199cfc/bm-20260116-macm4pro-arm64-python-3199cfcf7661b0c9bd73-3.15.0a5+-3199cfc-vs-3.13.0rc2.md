# Results vs. 3.13.0rc2

- fork: python
- ref: 3199cfcf7661b0c9bd73
- machine: darwin-arm64
- commit hash: 3199cfc
- commit date: 2026-01-16
- overall geometric mean: 1.057x faster
- HPT reliability: 99.66%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                    |
| sphinx         | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.33x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 224 ms: 2.32x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 228 ms: 1.77x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 239 ms: 1.62x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 105 ms: 1.36x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.35x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 141 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.7 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.4 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.18x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.0 ms: 1.12x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 46.1 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.77 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 47.0 ms: 1.02x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.1 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|---------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps          | 4.65 ms                                                        | 3.83 ms: 1.22x faster                                                    |
| xml_etree_iterparse | 46.1 ms                                                        | 39.3 ms: 1.17x faster                                                    |
| tomli_loads         | 1000 ms                                                        | 863 ms: 1.16x faster                                                     |
| xml_etree_parse     | 62.4 ms                                                        | 61.4 ms: 1.02x faster                                                    |
| xml_etree_generate  | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                    |
| json_loads          | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| pickle_pure_python  | 130 us                                                         | 143 us: 1.10x slower                                                     |
| Geometric mean      | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (2): unpickle_pure_python, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.81 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.34 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                    |
| mako            | 4.41 ms                                                        | 4.84 ms: 1.10x slower                                                    |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.33x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 224 ms: 2.32x faster                                                     |
| mdp                              | 1.06 sec                                                       | 554 ms: 1.91x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 228 ms: 1.77x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 239 ms: 1.62x faster                                                     |
| k_core                           | 1.46 sec                                                       | 906 ms: 1.62x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.10 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 101 us: 1.44x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 105 ms: 1.36x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.35x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 141 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.30x faster                                                     |
| go                               | 72.6 ms                                                        | 56.2 ms: 1.29x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.1 ms: 1.28x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.83 ms: 1.22x faster                                                    |
| pyflate                          | 222 ms                                                         | 187 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.18x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.10 us: 1.18x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.3 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.17x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 863 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| float                            | 31.4 ms                                                        | 28.0 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.77 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 924 us: 1.07x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.86 ms: 1.07x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.8 ms: 1.06x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.5 ms: 1.05x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.6 ms: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.7 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| fannkuch                         | 179 ms                                                         | 173 ms: 1.03x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 121 ms: 1.02x faster                                                     |
| sphinx                           | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 47.0 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 61.4 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 320 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.61 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.1 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.81 ms: 1.02x slower                                                    |
| thrift                           | 309 us                                                         | 316 us: 1.02x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.29 us: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.83 ms: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.51 us: 1.03x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 45.0 ms: 1.03x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 977 ns: 1.03x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.3 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.0 ms: 1.04x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.53 ms: 1.05x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.6 ms: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 437 us: 1.06x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 39.6 ms: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.2 ns: 1.06x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.34 ms: 1.07x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 103 ms: 1.08x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.32 us: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 117 ms: 1.08x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.5 ms: 1.08x slower                                                    |
| nbody                            | 42.5 ms                                                        | 46.1 ms: 1.08x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 46.7 ms: 1.09x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.84 ms: 1.10x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.1 ms: 1.10x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                     |
| connected_components             | 208 ms                                                         | 235 ms: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 45.3 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| many_optionals                   | 200 us                                                         | 257 us: 1.28x slower                                                     |
| generators                       | 15.7 ms                                                        | 20.4 ms: 1.30x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.4 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (7): typing_runtime_protocols, hexiom, pprint_pformat, unpickle_pure_python, genshi_text, xml_etree_process, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260116-3.15.0a5+-3199cfc/bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.057x faster

# HPT report

- Reliability score: 99.66% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x