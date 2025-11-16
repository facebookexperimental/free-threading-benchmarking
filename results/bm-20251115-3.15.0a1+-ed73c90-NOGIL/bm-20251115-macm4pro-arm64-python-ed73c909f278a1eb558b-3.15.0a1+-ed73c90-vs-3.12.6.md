# Results vs. 3.12.6

- fork: python
- ref: ed73c909f278a1eb558b
- machine: darwin-arm64
- commit hash: ed73c90
- commit date: 2025-11-15
- overall geometric mean: 1.103x faster
- HPT reliability: 99.87%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| docutils       | 1.02 sec                                                 | 996 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 416 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.45x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 193 ms: 2.31x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 86.3 ms: 1.99x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.3 ms: 1.80x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.72x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 238 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.6 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.4 ms: 2.41x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.5 ms: 1.38x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 55.2 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.9 ms: 1.07x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.4 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.33 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.5 ms: 1.38x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.2 ms: 1.17x faster                                                    |
| tomli_loads          | 957 ms                                                   | 891 ms: 1.07x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.97 ms: 1.07x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.78 ms: 1.22x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.09 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.3 ms: 1.07x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.08x slower                                                    |
| django_template | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                    |
| mako            | 4.77 ms                                                  | 5.68 ms: 1.19x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 773 us: 2.60x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.45x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 193 ms: 2.31x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 86.3 ms: 1.99x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                     |
| mdp                              | 1.09 sec                                                 | 605 ms: 1.81x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.3 ms: 1.80x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 479 us: 1.73x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.72x faster                                                     |
| deepcopy                         | 161 us                                                   | 109 us: 1.49x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 238 ms: 1.42x faster                                                     |
| float                            | 37.9 ms                                                  | 27.5 ms: 1.38x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.5 ms: 1.38x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.20 us: 1.21x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.11 us: 1.21x faster                                                    |
| go                               | 70.0 ms                                                  | 59.1 ms: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 825 ns: 1.17x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 58.2 ms: 1.17x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.9 ns: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                     |
| pylint                           | 128 ms                                                   | 113 ms: 1.13x faster                                                     |
| generators                       | 21.9 ms                                                  | 19.4 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.12x faster                                                   |
| raytrace                         | 145 ms                                                   | 129 ms: 1.12x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                    |
| pyflate                          | 216 ms                                                   | 193 ms: 1.12x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 18.9 ms: 1.10x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 49.8 ms: 1.09x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 56.0 ms: 1.09x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 891 ms: 1.07x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.97 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 464 ms: 1.07x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 50.9 ms: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.07x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.43 us: 1.06x faster                                                    |
| sphinx                           | 434 ms                                                   | 416 ms: 1.04x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.70 us: 1.04x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.9 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.4 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.33 ms: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 996 ms: 1.03x faster                                                     |
| fannkuch                         | 176 ms                                                   | 173 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                     |
| richards                         | 22.4 ms                                                  | 22.3 ms: 1.00x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 3.06 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody                            | 54.2 ms                                                  | 55.2 ms: 1.02x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 25.9 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.7 us: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 341 ms: 1.04x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.6 ms: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                     |
| thrift                           | 322 us                                                   | 337 us: 1.05x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 697 ms: 1.05x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.8 ms: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.5 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                     |
| dask                             | 528 ms                                                   | 560 ms: 1.06x slower                                                     |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.3 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.5 ms: 1.09x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 56.5 ms: 1.10x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.34 ms: 1.13x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.1 ms: 1.16x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.7 ms: 1.17x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.07 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.68 ms: 1.19x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.78 ms: 1.22x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.09 ms: 1.24x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 558 us: 1.33x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.6 ms: 1.51x slower                                                    |
| many_optionals                   | 195 us                                                   | 377 us: 1.93x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.4 ms: 2.41x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (2): nqueens, sympy_integrate
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251115-3.15.0a1+-ed73c90-NOGIL/bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.103x faster

# HPT report

- Reliability score: 99.87% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.36x