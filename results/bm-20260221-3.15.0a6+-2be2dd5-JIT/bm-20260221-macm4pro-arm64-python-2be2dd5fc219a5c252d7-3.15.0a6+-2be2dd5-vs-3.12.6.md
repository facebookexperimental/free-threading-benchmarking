# Results vs. 3.12.6

- fork: python
- ref: 2be2dd5fc219a5c252d7
- machine: darwin-arm64
- commit hash: 2be2dd5
- commit date: 2026-02-21
- overall geometric mean: 1.246x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 20.2 ms: 1.14x faster                                                    |
| sphinx         | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 222 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 231 ms: 2.08x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 226 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 224 ms: 1.99x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 98.2 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.3 ms: 1.77x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 134 ms: 1.66x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.26x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 37.3 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 123 ms: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.8 ms: 2.52x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.33x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 23.4 ms: 1.62x faster                                                    |
| nbody          | 54.2 ms                                                  | 40.0 ms: 1.36x faster                                                    |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                    | 1.28x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 40.8 ms: 1.34x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.9 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 656 ms: 1.46x faster                                                     |
| xml_etree_iterparse  | 51.6 ms                                                  | 37.8 ms: 1.36x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 31.1 ms: 1.25x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 22.1 ms: 1.21x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 86.3 us: 1.19x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.58 ms: 1.19x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.4 ms: 1.16x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 128 us: 1.09x faster                                                     |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.21x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.10 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.57 ms: 1.15x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.00 ms: 1.19x faster                                                    |
| django_template | 13.6 ms                                                  | 13.7 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.09x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.68 ms: 5.64x faster                                                    |
| richards                         | 22.4 ms                                                  | 9.42 ms: 2.38x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 11.2 ms: 2.27x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 222 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 231 ms: 2.08x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 226 ms: 2.03x faster                                                     |
| mdp                              | 1.09 sec                                                 | 544 ms: 2.01x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 224 ms: 1.99x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 98.2 ms: 1.82x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 28.4 ms: 1.80x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.3 ms: 1.77x faster                                                    |
| deepcopy                         | 161 us                                                   | 95.3 us: 1.69x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 10.8 us: 1.69x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 5.87 us: 1.68x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 134 ms: 1.66x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                     |
| float                            | 37.9 ms                                                  | 23.4 ms: 1.62x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 39.2 ms: 1.56x faster                                                    |
| go                               | 70.0 ms                                                  | 47.1 ms: 1.49x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 34.4 ns: 1.48x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.17 ms: 1.48x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 656 ms: 1.46x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 98.4 ms: 1.44x faster                                                    |
| pyflate                          | 216 ms                                                   | 151 ms: 1.43x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.42x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 38.7 ms: 1.40x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 23.2 ms: 1.39x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.8 ms: 1.36x faster                                                    |
| nbody                            | 54.2 ms                                                  | 40.0 ms: 1.36x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 40.8 ms: 1.34x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| chaos                            | 28.9 ms                                                  | 22.0 ms: 1.32x faster                                                    |
| raytrace                         | 145 ms                                                   | 112 ms: 1.30x faster                                                     |
| k_core                           | 1.12 sec                                                 | 866 ms: 1.29x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 33.7 ms: 1.29x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 524 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.26x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.42 ms: 1.26x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 31.1 ms: 1.25x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 263 ms: 1.24x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 37.3 ms: 1.22x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.84 sec: 1.22x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 22.1 ms: 1.21x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 32.1 ms: 1.21x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.14 us: 1.20x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.00 ms: 1.19x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 86.3 us: 1.19x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.35 us: 1.19x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.58 ms: 1.19x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.4 ms: 1.16x faster                                                    |
| fannkuch                         | 176 ms                                                   | 153 ms: 1.15x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 20.2 ms: 1.14x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.3 ms: 1.14x faster                                                    |
| pycparser                        | 497 ms                                                   | 438 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.85 ms: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.1 us: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                     |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 128 us: 1.09x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.47 ms: 1.07x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 54.4 ms: 1.06x faster                                                    |
| thrift                           | 322 us                                                   | 306 us: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| sympy_str                        | 104 ms                                                   | 99.5 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.9 ms: 1.04x faster                                                    |
| json                             | 1.93 ms                                                  | 1.86 ms: 1.04x faster                                                    |
| meteor_contest                   | 47.7 ms                                                  | 46.1 ms: 1.04x faster                                                    |
| connected_components             | 201 ms                                                   | 196 ms: 1.02x faster                                                     |
| shortest_path                    | 219 ms                                                   | 215 ms: 1.02x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 953 ns: 1.02x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| telco                            | 2.61 ms                                                  | 2.59 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                     |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                     |
| django_template                  | 13.6 ms                                                  | 13.7 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 433 us: 1.03x slower                                                     |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.11 ms: 1.05x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 123 ms: 1.09x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.10 ms: 1.14x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 949 us: 1.14x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.57 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 46.7 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.4 ms: 1.24x slower                                                    |
| many_optionals                   | 195 us                                                   | 244 us: 1.25x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.8 ms: 2.52x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260221-3.15.0a6+-2be2dd5-JIT/bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.246x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.12x

# Memory
- memory change: 1.27x