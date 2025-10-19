# Results vs. 3.13.0rc2

- fork: python
- ref: bedaea05987738c4c6b9
- machine: darwin-arm64
- commit hash: bedaea0
- commit date: 2025-10-19
- overall geometric mean: 1.025x faster
- HPT reliability: 95.07%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 249 ms: 2.09x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.55x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 260 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.2 ms: 2.98x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 49.1 ms: 1.15x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.41 ms: 1.15x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.68 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 94.0 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 48.9 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.86 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 903 ms: 1.11x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.0 ms: 1.07x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.9 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.5 ms: 1.01x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 100 us: 1.01x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (2): xml_etree_process, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.34 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.1 ms: 1.03x slower                                                    |
| mako            | 4.41 ms                                                        | 4.78 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 249 ms: 2.09x faster                                                     |
| mdp                              | 1.06 sec                                                       | 542 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.55x faster                                                     |
| k_core                           | 1.46 sec                                                       | 989 ms: 1.48x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.0 us: 1.37x faster                                                    |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                     |
| go                               | 72.6 ms                                                        | 56.2 ms: 1.29x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 51.3 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.86 ms: 1.20x faster                                                    |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.41 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 260 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 903 ms: 1.11x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.68 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.08x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.0 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.87 ms: 1.07x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 934 us: 1.06x faster                                                     |
| float                            | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.1 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.9 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 63.3 us: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.38 ms: 1.02x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.6 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 24.5 ms: 1.01x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.5 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.7 ms: 1.01x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 94.0 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 100 us: 1.01x slower                                                     |
| 2to3                             | 112 ms                                                         | 112 ms: 1.01x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 44.1 ms: 1.01x slower                                                    |
| thrift                           | 309 us                                                         | 312 us: 1.01x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 659 ms: 1.01x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 37.8 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 327 ms: 1.02x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 48.9 ms: 1.02x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                    |
| pycparser                        | 470 ms                                                         | 484 ms: 1.03x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 22.1 ms: 1.03x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.04x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.4 ns: 1.04x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.36 us: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.59 us: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.34 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.7 ms: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.90 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                     |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.07x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.78 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.45 us: 1.09x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.2 ms: 1.11x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 42.4 ms: 1.12x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.9 ms: 1.14x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 49.0 ms: 1.15x slower                                                    |
| nbody                            | 42.5 ms                                                        | 49.1 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| many_optionals                   | 200 us                                                         | 365 us: 1.82x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 17.6 ms: 2.82x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.2 ms: 2.98x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (9): sphinx, sqlite_synth, genshi_text, hexiom, xml_etree_process, bench_thread_pool, gc_traversal, json_loads, fannkuch
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251019-3.15.0a1+-bedaea0/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.025x faster

# HPT report

- Reliability score: 95.07% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.15x