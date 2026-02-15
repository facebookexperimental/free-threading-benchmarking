# Results vs. 3.13.0rc2

- fork: python
- ref: 645f5c4a737b3eab29d0
- machine: darwin-arm64
- commit hash: 645f5c4
- commit date: 2026-02-14
- overall geometric mean: 1.023x faster
- HPT reliability: 70.22%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.08x slower                                                     |
| docutils       | 1.05 sec                                                       | 999 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.7 ms: 1.02x faster                                                    |
| sphinx         | 409 ms                                                         | 416 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 241 ms: 2.16x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 237 ms: 1.71x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                     |
| async_generators                 | 193 ms                                                         | 185 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.4 ms: 3.19x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 55.2 ms: 1.30x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.25 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.4 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.4 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.87 ms: 1.20x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.2 ms: 1.18x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 870 ms: 1.15x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.4 ms: 1.07x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.02x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.6 ms: 1.05x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 107 us: 1.07x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.73 ms: 1.13x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.13 ms: 1.20x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                    |
| mako            | 4.41 ms                                                        | 5.46 ms: 1.24x slower                                                    |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 788 us: 2.59x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 241 ms: 2.16x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 503 us: 1.97x faster                                                     |
| mdp                              | 1.06 sec                                                       | 602 ms: 1.76x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 237 ms: 1.71x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.11 ms: 1.52x faster                                                    |
| k_core                           | 1.46 sec                                                       | 990 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 105 us: 1.38x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| go                               | 72.6 ms                                                        | 59.8 ms: 1.21x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 789 ns: 1.20x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.87 ms: 1.20x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 53.9 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.2 ms: 1.18x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.25 ms: 1.16x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 870 ms: 1.15x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.12x faster                                                    |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 58.4 ms: 1.07x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.03 sec: 1.05x faster                                                   |
| docutils                         | 1.05 sec                                                       | 999 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 185 ms: 1.05x faster                                                     |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.97 ms: 1.03x faster                                                    |
| pycparser                        | 470 ms                                                         | 456 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.7 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.4 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 323 ms: 1.00x slower                                                     |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 659 ms: 1.01x slower                                                     |
| sphinx                           | 409 ms                                                         | 416 ms: 1.02x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                    |
| richards                         | 22.1 ms                                                        | 22.9 ms: 1.04x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.6 ms: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.4 ms: 1.05x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.1 ms: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.0 ns: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.03 ms: 1.07x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.39 us: 1.07x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 107 us: 1.07x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.63 us: 1.08x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.3 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| 2to3                             | 112 ms                                                         | 121 ms: 1.08x slower                                                     |
| thrift                           | 309 us                                                         | 338 us: 1.09x slower                                                     |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.11x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.12x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 72.8 us: 1.13x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.73 ms: 1.13x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.5 ms: 1.13x slower                                                    |
| shortest_path                    | 225 ms                                                         | 255 ms: 1.13x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 54.4 ms: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 43.0 ms: 1.15x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.5 ms: 1.16x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.6 ms: 1.16x slower                                                    |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.13 ms: 1.20x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.14 ms: 1.20x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.29 us: 1.22x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.4 ms: 1.23x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.6 ms: 1.23x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.46 ms: 1.24x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 42.5 ms: 1.26x slower                                                    |
| nbody                            | 42.5 ms                                                        | 55.2 ms: 1.30x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 56.1 ms: 1.31x slower                                                    |
| many_optionals                   | 200 us                                                         | 266 us: 1.33x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 548 us: 1.33x slower                                                     |
| generators                       | 15.7 ms                                                        | 21.1 ms: 1.34x slower                                                    |
| connected_components             | 208 ms                                                         | 303 ms: 1.46x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.4 ms: 3.19x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (2): json, scimark_fft
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260214-3.15.0a6+-645f5c4-NOGIL/bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.023x faster

# HPT report

- Reliability score: 70.22% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.30x