# Results vs. 3.12.6

- fork: python
- ref: 2be2dd5fc219a5c252d7
- machine: darwin-arm64
- commit hash: 2be2dd5
- commit date: 2026-02-21
- overall geometric mean: 1.164x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 114 ms: 1.00x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 21.6 ms: 1.07x faster                                                    |
| sphinx         | 434 ms                                                   | 392 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 226 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.10x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 226 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 97.1 ms: 1.77x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.64x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 39.9 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.8 ms: 2.51x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.33x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| nbody          | 54.2 ms                                                  | 46.2 ms: 1.17x faster                                                    |
| pidigits       | 161 ms                                                   | 170 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                    | 1.14x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.8 ms: 1.25x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.94 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.1 ms: 1.29x faster                                                    |
| tomli_loads          | 957 ms                                                   | 783 ms: 1.22x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 32.8 ms: 1.19x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.72 ms: 1.15x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 23.5 ms: 1.14x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 93.9 us: 1.10x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 64.8 ms: 1.05x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 136 us: 1.02x faster                                                     |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.12 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.56 ms: 1.15x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.12 ms: 1.15x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 19.8 ms: 1.10x faster                                                    |
| django_template | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.06x faster                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.95 ms: 5.25x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 226 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.10x faster                                                     |
| mdp                              | 1.09 sec                                                 | 526 ms: 2.08x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 226 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 97.1 ms: 1.77x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| deepcopy                         | 161 us                                                   | 96.3 us: 1.68x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.64x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.4 us: 1.60x faster                                                    |
| generators                       | 21.9 ms                                                  | 14.9 ms: 1.48x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.42x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.98 us: 1.41x faster                                                    |
| go                               | 70.0 ms                                                  | 51.8 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| float                            | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.1 ms: 1.29x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.4 ms: 1.25x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 43.8 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.6 ms: 1.23x faster                                                    |
| k_core                           | 1.12 sec                                                 | 911 ms: 1.23x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 41.6 ns: 1.22x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 783 ms: 1.22x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 32.8 ms: 1.19x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.6 ms: 1.18x faster                                                    |
| nbody                            | 54.2 ms                                                  | 46.2 ms: 1.17x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 43.8 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.43 us: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.12 ms: 1.15x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 123 ms: 1.15x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.72 ms: 1.15x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.9 ms: 1.14x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 23.5 ms: 1.14x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.3 ms: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.13x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.68 ms: 1.13x faster                                                    |
| pyflate                          | 216 ms                                                   | 192 ms: 1.13x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 22.6 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                     |
| richards                         | 22.4 ms                                                  | 20.1 ms: 1.12x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.7 us: 1.12x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 392 ms: 1.11x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 19.8 ms: 1.10x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.3 ms: 1.10x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 93.9 us: 1.10x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.45 ms: 1.08x faster                                                    |
| thrift                           | 322 us                                                   | 301 us: 1.07x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.6 ms: 1.07x faster                                                    |
| sympy_str                        | 104 ms                                                   | 98.2 ms: 1.06x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 54.5 ms: 1.06x faster                                                    |
| pycparser                        | 497 ms                                                   | 471 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 64.8 ms: 1.05x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 315 ms: 1.04x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 640 ms: 1.04x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 935 ns: 1.03x faster                                                     |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 136 us: 1.02x faster                                                     |
| sympy_expand                     | 167 ms                                                   | 164 ms: 1.02x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.04 ms: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| bench_thread_pool                | 419 us                                                   | 414 us: 1.01x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| 2to3                             | 114 ms                                                   | 114 ms: 1.00x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 39.0 ms: 1.00x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| django_template                  | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.02x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.94 ms: 1.04x slower                                                    |
| shortest_path                    | 219 ms                                                   | 227 ms: 1.04x slower                                                     |
| pidigits                         | 161 ms                                                   | 170 ms: 1.05x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.3 ms: 1.05x slower                                                    |
| connected_components             | 201 ms                                                   | 212 ms: 1.06x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.14 ms: 1.06x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.83 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.12 ms: 1.14x slower                                                    |
| coverage                         | 26.9 ms                                                  | 30.8 ms: 1.15x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.56 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 963 us: 1.16x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 46.3 ms: 1.17x slower                                                    |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.8 ms: 2.51x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |

Benchmark hidden because not significant (3): mako, asyncio_websockets, regex_dna
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260221-3.15.0a6+-2be2dd5-CLANG/bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.164x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.21x