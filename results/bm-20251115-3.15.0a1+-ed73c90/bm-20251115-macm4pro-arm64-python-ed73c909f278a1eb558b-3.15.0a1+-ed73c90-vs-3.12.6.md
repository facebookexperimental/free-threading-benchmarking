# Results vs. 3.12.6

- fork: python
- ref: ed73c909f278a1eb558b
- machine: darwin-arm64
- commit hash: ed73c90
- commit date: 2025-11-15
- overall geometric mean: 1.144x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 22.0 ms: 1.05x faster                                                    |
| sphinx         | 434 ms                                                   | 395 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 221 ms: 2.17x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 227 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 98.6 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.6 ms: 1.76x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.68x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.96 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 251 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| async_generators                 | 206 ms                                                   | 171 ms: 1.20x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.8 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 124 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.3 ms: 2.50x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.33x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.7 ms: 1.42x faster                                                    |
| nbody          | 54.2 ms                                                  | 45.3 ms: 1.20x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.19x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.1 ms: 1.18x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.6 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.0 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| tomli_loads          | 957 ms                                                   | 837 ms: 1.14x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.83 ms: 1.11x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.1 ms: 1.11x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 96.1 us: 1.07x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.88 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.70 ms: 1.08x faster                                                    |
| mako            | 4.77 ms                                                  | 4.59 ms: 1.04x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 221 ms: 2.17x faster                                                     |
| mdp                              | 1.09 sec                                                 | 529 ms: 2.06x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 227 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 98.6 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.6 ms: 1.76x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.68x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.1 us: 1.65x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| deepcopy                         | 161 us                                                   | 101 us: 1.59x faster                                                     |
| float                            | 37.9 ms                                                  | 26.7 ms: 1.42x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.09 us: 1.39x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.96 ms: 1.36x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.08 us: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 251 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| go                               | 70.0 ms                                                  | 52.9 ms: 1.32x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 41.2 ns: 1.24x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.1 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 50.1 ms: 1.22x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 118 ms: 1.21x faster                                                     |
| async_generators                 | 206 ms                                                   | 171 ms: 1.20x faster                                                     |
| nbody                            | 54.2 ms                                                  | 45.3 ms: 1.20x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.4 ms: 1.19x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                    |
| pyflate                          | 216 ms                                                   | 182 ms: 1.18x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 46.1 ms: 1.18x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.6 ms: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.77 ms: 1.17x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.21 us: 1.17x faster                                                    |
| pylint                           | 128 ms                                                   | 111 ms: 1.16x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.44 us: 1.15x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.1 ms: 1.15x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 837 ms: 1.14x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.7 us: 1.13x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.7 ms: 1.12x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.8 ms: 1.12x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.83 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.1 ms: 1.11x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.74 ms: 1.11x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.9 ms: 1.11x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.4 ms: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 395 ms: 1.10x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 46.8 ms: 1.10x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.70 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 461 ms: 1.08x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.45 ms: 1.08x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 96.1 us: 1.07x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 36.4 ms: 1.07x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 628 ms: 1.06x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 94.6 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.0 ms: 1.05x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 313 ms: 1.05x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.59 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                     |
| thrift                           | 322 us                                                   | 310 us: 1.04x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.5 ms: 1.04x faster                                                    |
| fannkuch                         | 176 ms                                                   | 171 ms: 1.03x faster                                                     |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 48.5 ms: 1.02x slower                                                    |
| dask                             | 528 ms                                                   | 540 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.03x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.06 ms: 1.03x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.0 ms: 1.05x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.85 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 124 ms: 1.10x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 43.8 ms: 1.10x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 918 us: 1.11x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.88 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.13x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.3 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 351 us: 1.80x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.3 ms: 2.50x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                             |

Benchmark hidden because not significant (3): sqlite_synth, json_loads, json
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251115-3.15.0a1+-ed73c90/bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.144x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.23x