# Results vs. 3.12.6

- fork: python
- ref: a936af924efc6e2fb59e
- machine: darwin-arm64
- commit hash: a936af9
- commit date: 2025-03-17
- overall geometric mean: 1.075x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.02x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                   |
| html5lib       | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 414 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 257 ms: 1.93x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 260 ms: 1.85x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 266 ms: 1.73x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 260 ms: 1.71x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.58x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 153 ms: 1.50x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 155 ms: 1.44x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.14x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 43.1 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 136 ms: 1.21x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 90.4 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.5 ms: 1.17x faster                                                    |
| nbody          | 54.2 ms                                                  | 50.1 ms: 1.08x faster                                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 48.5 ms: 1.13x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 91.8 ms: 1.09x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.7 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 46.2 ms: 1.12x faster                                                    |
| tomli_loads          | 957 ms                                                   | 867 ms: 1.10x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 63.0 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 104 us: 1.01x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 4.97 ms: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.59 ms: 1.07x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.38 ms: 1.12x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 21.6 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                             |

Benchmark hidden because not significant (2): genshi_text, mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.59 ms: 2.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 257 ms: 1.93x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 260 ms: 1.85x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 266 ms: 1.73x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 260 ms: 1.71x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.58x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 153 ms: 1.50x faster                                                     |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 155 ms: 1.44x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.71 us: 1.28x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.5 ms: 1.22x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.3 ms: 1.20x faster                                                    |
| go                               | 70.0 ms                                                  | 58.4 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.18x faster                                                     |
| float                            | 37.9 ms                                                  | 32.5 ms: 1.17x faster                                                    |
| raytrace                         | 145 ms                                                   | 124 ms: 1.16x faster                                                     |
| k_core                           | 1.12 sec                                                 | 963 ms: 1.16x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.0 ns: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.14x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.0 ms: 1.13x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.5 ms: 1.13x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 48.6 ms: 1.12x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 46.2 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 867 ms: 1.10x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.06 sec: 1.09x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.59 ms: 1.09x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 91.8 ms: 1.09x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.59 us: 1.08x faster                                                    |
| nbody                            | 54.2 ms                                                  | 50.1 ms: 1.08x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.92 ms: 1.08x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.0 ms: 1.08x faster                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 36.8 ms: 1.08x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.07x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.39 us: 1.07x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.1 ms: 1.06x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 67.2 us: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| pyflate                          | 216 ms                                                   | 206 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| sphinx                           | 434 ms                                                   | 414 ms: 1.05x faster                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 44.6 ms: 1.05x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.8 ms: 1.04x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 31.3 ms: 1.03x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.96 ms: 1.03x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.1 ms: 1.03x faster                                                    |
| 2to3                             | 114 ms                                                   | 111 ms: 1.02x faster                                                     |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 948 ns: 1.02x faster                                                     |
| thrift                           | 322 us                                                   | 316 us: 1.02x faster                                                     |
| sqlglot_parse                    | 577 us                                                   | 569 us: 1.02x faster                                                     |
| pycparser                        | 497 ms                                                   | 492 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 50.7 ms: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.6 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| sqlglot_transpile                | 696 us                                                   | 691 us: 1.01x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 43.2 ms: 1.01x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 662 ms: 1.00x faster                                                     |
| shortest_path                    | 219 ms                                                   | 220 ms: 1.00x slower                                                     |
| sqlglot_optimize                 | 23.4 ms                                                  | 23.5 ms: 1.00x slower                                                    |
| sqlglot_normalize                | 126 ms                                                   | 126 ms: 1.01x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 104 us: 1.01x slower                                                     |
| richards                         | 22.4 ms                                                  | 22.7 ms: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.13 ms: 1.01x slower                                                    |
| connected_components             | 201 ms                                                   | 204 ms: 1.01x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.25 ms: 1.02x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 171 ms: 1.02x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.06 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.1 ms: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 40.1 ms: 1.03x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 433 us: 1.03x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 882 us: 1.06x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.59 ms: 1.07x slower                                                    |
| fannkuch                         | 176 ms                                                   | 189 ms: 1.08x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 10.7 ms: 1.12x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.38 ms: 1.12x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 4.97 ms: 1.17x slower                                                    |
| many_optionals                   | 195 us                                                   | 232 us: 1.19x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.0 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 136 ms: 1.21x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.27 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 90.4 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (6): mdp, richards_super, pprint_safe_repr, genshi_text, mako, asyncio_websockets
Ignored benchmarks (4) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, tornado_http

- Geometric mean (including insignificant results): 1.075x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.11x