# Results vs. 3.12.6

- fork: python
- ref: dd88e77fad887aaf00ea
- machine: darwin-arm64
- commit hash: dd88e77
- commit date: 2026-04-10
- overall geometric mean: 1.106x faster
- HPT reliability: 99.93%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| docutils       | 1.02 sec                                                 | 968 ms: 1.06x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                    |
| sphinx         | 434 ms                                                   | 414 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 245 ms: 1.87x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.86x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.61x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.53x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                     |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.1 ms: 1.03x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.7 ms: 2.88x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.02x faster                                                     |
| nbody          | 54.2 ms                                                  | 55.9 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.3 ms: 1.09x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.1 ms: 1.07x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.03 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.5 ms: 1.18x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.82 ms: 1.11x faster                                                    |
| tomli_loads          | 957 ms                                                   | 864 ms: 1.11x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.03x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.04x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.68 ms: 1.21x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.05 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.13x slower                                                    |
| mako            | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.11 ms: 5.06x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 787 us: 2.55x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 245 ms: 1.87x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.86x faster                                                     |
| mdp                              | 1.09 sec                                                 | 600 ms: 1.82x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 509 us: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.61x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.53x faster                                                     |
| deepcopy                         | 161 us                                                   | 106 us: 1.52x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.4 us: 1.48x faster                                                    |
| float                            | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 783 ns: 1.23x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.11 us: 1.21x faster                                                    |
| go                               | 70.0 ms                                                  | 58.6 ms: 1.19x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.0 ns: 1.18x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.5 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                    |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                     |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 988 ms: 1.13x faster                                                     |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.82 ms: 1.11x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 864 ms: 1.11x faster                                                     |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 55.3 ms: 1.10x faster                                                    |
| pycparser                        | 497 ms                                                   | 452 ms: 1.10x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.34 us: 1.10x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.9 ms: 1.09x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 50.3 ms: 1.09x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.59 us: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.3 ms: 1.08x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.0 ms: 1.07x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.1 ms: 1.07x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.03 ms: 1.06x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.7 ms: 1.06x faster                                                    |
| docutils                         | 1.02 sec                                                 | 968 ms: 1.06x faster                                                     |
| sphinx                           | 434 ms                                                   | 414 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                    |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                     |
| pidigits                         | 161 ms                                                   | 159 ms: 1.02x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.96 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 329 ms: 1.00x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 673 ms: 1.01x slower                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 72.4 us: 1.02x slower                                                    |
| richards                         | 22.4 ms                                                  | 22.9 ms: 1.02x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.1 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.13 ms: 1.03x slower                                                    |
| nbody                            | 54.2 ms                                                  | 55.9 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.1 ms: 1.03x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.3 ms: 1.04x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.0 ms: 1.04x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.04x slower                                                     |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.06x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 54.6 ms: 1.06x slower                                                    |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| thrift                           | 322 us                                                   | 345 us: 1.07x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.27 ms: 1.09x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.11x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 43.6 ms: 1.12x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.14x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 54.6 ms: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                    |
| shortest_path                    | 219 ms                                                   | 253 ms: 1.16x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 47.3 ms: 1.19x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.68 ms: 1.21x slower                                                    |
| connected_components             | 201 ms                                                   | 243 ms: 1.21x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.05 ms: 1.24x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 565 us: 1.35x slower                                                     |
| many_optionals                   | 195 us                                                   | 264 us: 1.35x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.3 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.7 ms: 2.88x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (3): json, xml_etree_process, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260410-3.15.0a8+-dd88e77-NOGIL/bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.106x faster

# HPT report

- Reliability score: 99.93% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.38x