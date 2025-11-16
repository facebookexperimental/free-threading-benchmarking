# Results vs. 3.12.6

- fork: python
- ref: ed73c909f278a1eb558b
- machine: darwin-arm64
- commit hash: ed73c90
- commit date: 2025-11-15
- overall geometric mean: 1.158x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.03x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.00x slower                                                   |
| html5lib       | 23.0 ms                                                  | 21.1 ms: 1.09x faster                                                    |
| sphinx         | 434 ms                                                   | 390 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.25x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 218 ms: 2.20x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 226 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 98.1 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 96.9 ms: 1.78x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.60x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 39.8 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 124 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.9 ms: 2.49x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.33x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| nbody          | 54.2 ms                                                  | 47.2 ms: 1.15x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.16x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.7 ms: 1.25x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 98.2 ms: 1.01x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.3 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.9 ms: 1.32x faster                                                    |
| tomli_loads          | 957 ms                                                   | 773 ms: 1.24x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 32.6 ms: 1.19x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 23.5 ms: 1.14x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 91.7 us: 1.12x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 62.5 ms: 1.09x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 135 us: 1.03x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.14x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.74 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.40 ms: 1.12x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.2 ms: 1.08x faster                                                    |
| mako            | 4.77 ms                                                  | 4.62 ms: 1.03x faster                                                    |
| django_template | 13.6 ms                                                  | 14.1 ms: 1.03x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.05x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.25x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 218 ms: 2.20x faster                                                     |
| mdp                              | 1.09 sec                                                 | 521 ms: 2.09x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 226 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 98.1 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 96.9 ms: 1.78x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| deepcopy                         | 161 us                                                   | 97.0 us: 1.66x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.1 us: 1.65x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.60x faster                                                     |
| generators                       | 21.9 ms                                                  | 14.5 ms: 1.51x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.85 us: 1.44x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.41x faster                                                    |
| go                               | 70.0 ms                                                  | 51.0 ms: 1.37x faster                                                    |
| float                            | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.9 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 43.7 ms: 1.25x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 773 ms: 1.24x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.2 ms: 1.24x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.9 ns: 1.21x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.43 ms: 1.21x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.1 ms: 1.21x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.4 ms: 1.19x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 32.6 ms: 1.19x faster                                                    |
| pylint                           | 128 ms                                                   | 108 ms: 1.19x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 43.3 ms: 1.19x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.17 us: 1.18x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.58 ms: 1.18x faster                                                    |
| richards                         | 22.4 ms                                                  | 19.1 ms: 1.18x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.39 us: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 121 ms: 1.17x faster                                                     |
| pyflate                          | 216 ms                                                   | 185 ms: 1.17x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.1 ms: 1.15x faster                                                    |
| nbody                            | 54.2 ms                                                  | 47.2 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 39.8 ms: 1.15x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 23.5 ms: 1.14x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.5 ms: 1.14x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.7 ms: 1.12x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.7 ms: 1.12x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 91.7 us: 1.12x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.85 ms: 1.12x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.5 us: 1.12x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.40 ms: 1.12x faster                                                    |
| sphinx                           | 434 ms                                                   | 390 ms: 1.11x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| pycparser                        | 497 ms                                                   | 452 ms: 1.10x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.33 ms: 1.09x faster                                                    |
| thrift                           | 322 us                                                   | 295 us: 1.09x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.1 ms: 1.09x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 62.5 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 615 ms: 1.08x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 20.2 ms: 1.08x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 303 ms: 1.08x faster                                                     |
| sympy_str                        | 104 ms                                                   | 97.0 ms: 1.07x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 53.6 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| 2to3                             | 114 ms                                                   | 110 ms: 1.03x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.6 ms: 1.03x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.62 ms: 1.03x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 135 us: 1.03x faster                                                     |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 163 ms: 1.03x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 98.2 ms: 1.01x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 957 ns: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| bench_thread_pool                | 419 us                                                   | 416 us: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.00x slower                                                   |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| dask                             | 528 ms                                                   | 538 ms: 1.02x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 48.8 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.06 ms: 1.03x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.1 ms: 1.03x slower                                                    |
| fannkuch                         | 176 ms                                                   | 182 ms: 1.04x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 10.3 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.83 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.74 ms: 1.09x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 43.4 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 124 ms: 1.10x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 927 us: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.3 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 349 us: 1.79x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.9 ms: 2.49x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251115-3.15.0a1+-ed73c90-CLANG/bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.158x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.21x