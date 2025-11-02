# Results vs. 3.12.6

- fork: python
- ref: 2f60b8f02fe7cb83dd58
- machine: darwin-arm64
- commit hash: 2f60b8f
- commit date: 2025-11-01
- overall geometric mean: 1.116x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 402 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 229 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.12x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 229 ms: 2.01x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 229 ms: 1.95x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 142 ms: 1.57x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 42.6 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.8 ms: 2.58x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.31x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| nbody          | 54.2 ms                                                  | 47.9 ms: 1.13x faster                                                    |
| Geometric mean | (ref)                                                    | 1.15x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 48.2 ms: 1.13x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.78 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.5 ms: 1.27x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.8 ms: 1.09x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                    |
| tomli_loads          | 957 ms                                                   | 889 ms: 1.08x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                     |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.03x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.19 ms: 1.09x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.75 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.0 ms: 1.05x faster                                                    |
| mako            | 4.77 ms                                                  | 4.81 ms: 1.01x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 229 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.12x faster                                                     |
| mdp                              | 1.09 sec                                                 | 539 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 229 ms: 2.01x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 229 ms: 1.95x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 142 ms: 1.57x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.9 us: 1.54x faster                                                    |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| float                            | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 7.46 us: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.13 us: 1.29x faster                                                    |
| go                               | 70.0 ms                                                  | 54.9 ms: 1.28x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.5 ms: 1.27x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.1 ms: 1.26x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 48.6 ms: 1.25x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.6 ms: 1.25x faster                                                    |
| raytrace                         | 145 ms                                                   | 116 ms: 1.25x faster                                                     |
| k_core                           | 1.12 sec                                                 | 902 ms: 1.24x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 41.8 ns: 1.22x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.75 ms: 1.18x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 18.1 ms: 1.15x faster                                                    |
| pyflate                          | 216 ms                                                   | 189 ms: 1.15x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.4 ms: 1.14x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.2 ms: 1.13x faster                                                    |
| nbody                            | 54.2 ms                                                  | 47.9 ms: 1.13x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.5 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.32 us: 1.11x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.53 us: 1.11x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.2 ms: 1.11x faster                                                    |
| pylint                           | 128 ms                                                   | 117 ms: 1.10x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 39.6 ms: 1.10x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.8 ms: 1.09x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 47.3 ms: 1.09x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 402 ms: 1.08x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 889 ms: 1.08x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 66.0 us: 1.08x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.83 ms: 1.07x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.6 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.51 ms: 1.07x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.0 ms: 1.05x faster                                                    |
| pycparser                        | 497 ms                                                   | 477 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 24.5 ms: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.5 ms: 1.03x faster                                                    |
| thrift                           | 322 us                                                   | 312 us: 1.03x faster                                                     |
| richards                         | 22.4 ms                                                  | 21.8 ms: 1.03x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 56.5 ms: 1.02x faster                                                    |
| sympy_str                        | 104 ms                                                   | 103 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| bench_thread_pool                | 419 us                                                   | 414 us: 1.01x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 658 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 326 ms: 1.01x faster                                                     |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.81 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.78 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.05 ms: 1.02x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.03x slower                                                     |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                     |
| connected_components             | 201 ms                                                   | 208 ms: 1.04x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 41.2 ms: 1.04x slower                                                    |
| fannkuch                         | 176 ms                                                   | 183 ms: 1.04x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 174 ms: 1.04x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.8 ms: 1.04x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.19 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.75 ms: 1.09x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.88 ms: 1.10x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 922 us: 1.11x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.14x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.5 ms: 1.21x slower                                                    |
| many_optionals                   | 195 us                                                   | 363 us: 1.86x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.8 ms: 2.58x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                             |

Benchmark hidden because not significant (4): json_loads, pidigits, json, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251101-3.15.0a1+-2f60b8f/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.116x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.20x