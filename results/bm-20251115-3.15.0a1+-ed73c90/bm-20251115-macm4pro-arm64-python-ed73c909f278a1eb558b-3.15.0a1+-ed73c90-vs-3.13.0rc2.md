# Results vs. 3.13.0rc2

- fork: python
- ref: ed73c909f278a1eb558b
- machine: darwin-arm64
- commit hash: ed73c90
- commit date: 2025-11-15
- overall geometric mean: 1.055x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.00x faster                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                    |
| sphinx         | 409 ms                                                         | 395 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 223 ms: 2.36x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 223 ms: 2.34x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 221 ms: 1.83x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 227 ms: 1.70x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 98.6 ms: 1.44x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 97.6 ms: 1.36x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.35x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.96 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.8 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 124 ms: 1.21x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.3 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.7 ms: 1.18x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 45.3 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.14x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.1 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.83 ms: 1.22x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 837 ms: 1.19x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 96.1 us: 1.03x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.1 ms: 1.02x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.88 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.70 ms: 1.03x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| mako            | 4.41 ms                                                        | 4.59 ms: 1.04x slower                                                    |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 223 ms: 2.36x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 223 ms: 2.34x faster                                                     |
| mdp                              | 1.06 sec                                                       | 529 ms: 2.00x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 221 ms: 1.83x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 227 ms: 1.70x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.1 us: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 98.6 ms: 1.44x faster                                                    |
| deepcopy                         | 145 us                                                         | 101 us: 1.43x faster                                                     |
| go                               | 72.6 ms                                                        | 52.9 ms: 1.37x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 97.6 ms: 1.36x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.35x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.1 ms: 1.28x faster                                                    |
| pyflate                          | 222 ms                                                         | 182 ms: 1.22x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.83 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 837 ms: 1.19x faster                                                     |
| float                            | 31.4 ms                                                        | 26.7 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.08x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.4 ms: 1.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 918 us: 1.08x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.96 ms: 1.08x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.9 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.85 ms: 1.07x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.1 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.8 ms: 1.06x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 118 ms: 1.05x faster                                                     |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.05x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.74 ms: 1.04x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.1 ms: 1.04x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 628 ms: 1.04x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 96.1 us: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| sphinx                           | 409 ms                                                         | 395 ms: 1.03x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.7 us: 1.03x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.70 ms: 1.03x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 313 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 61.1 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| pycparser                        | 470 ms                                                         | 461 ms: 1.02x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.21 us: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.45 ms: 1.01x faster                                                    |
| 2to3                             | 112 ms                                                         | 111 ms: 1.00x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.44 us: 1.00x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.77 ms: 1.00x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.45 ms: 1.00x slower                                                    |
| thrift                           | 309 us                                                         | 310 us: 1.00x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 44.1 ms: 1.01x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.6 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.5 ms: 1.01x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.2 ns: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 966 ns: 1.02x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.88 ms: 1.03x slower                                                    |
| dask                             | 525 ms                                                         | 540 ms: 1.03x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.3 ms: 1.03x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.7 ms: 1.04x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.59 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.09 us: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.04x slower                                                     |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.5 ms: 1.06x slower                                                    |
| nbody                            | 42.5 ms                                                        | 45.3 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 36.4 ms: 1.08x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 46.8 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 43.8 ms: 1.16x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.17x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 124 ms: 1.21x slower                                                     |
| many_optionals                   | 200 us                                                         | 351 us: 1.75x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.3 ms: 2.77x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.4 ms: 2.79x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (3): regex_dna, json, json_loads
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251115-3.15.0a1+-ed73c90/bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.055x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.18x