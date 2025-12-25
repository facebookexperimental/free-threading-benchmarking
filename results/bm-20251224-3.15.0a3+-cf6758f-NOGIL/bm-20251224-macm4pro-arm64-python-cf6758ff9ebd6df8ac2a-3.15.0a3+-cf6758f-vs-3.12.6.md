# Results vs. 3.12.6

- fork: python
- ref: cf6758ff9ebd6df8ac2a
- machine: darwin-arm64
- commit hash: cf6758f
- commit date: 2025-12-24
- overall geometric mean: 1.096x faster
- HPT reliability: 98.86%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.01x faster                                                   |
| sphinx         | 434 ms                                                   | 426 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 237 ms: 2.02x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 250 ms: 1.98x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 249 ms: 1.85x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.65x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.48x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 257 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                     |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.5 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.8 ms: 2.89x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.6 ms: 1.33x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| nbody          | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.9 ms: 1.07x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.9 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.73 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.5 ms: 1.31x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.4 ms: 1.16x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.93 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.1 ms: 1.02x slower                                                    |
| tomli_loads          | 957 ms                                                   | 975 ms: 1.02x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 107 us: 1.04x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.05x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.81 ms: 1.22x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.12 ms: 1.25x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.24x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.2 ms: 1.06x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                    |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                    |
| mako            | 4.77 ms                                                  | 5.49 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.11x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.05 ms: 5.13x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 802 us: 2.51x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 237 ms: 2.02x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 250 ms: 1.98x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 249 ms: 1.85x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                     |
| mdp                              | 1.09 sec                                                 | 606 ms: 1.80x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.65x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 504 us: 1.65x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                     |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.48x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.45x faster                                                    |
| float                            | 37.9 ms                                                  | 28.6 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 257 ms: 1.32x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.5 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.24 us: 1.19x faster                                                    |
| go                               | 70.0 ms                                                  | 59.3 ms: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 821 ns: 1.18x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 58.4 ms: 1.16x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.9 ns: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 53.6 ms: 1.14x faster                                                    |
| raytrace                         | 145 ms                                                   | 128 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 994 ms: 1.12x faster                                                     |
| pyflate                          | 216 ms                                                   | 193 ms: 1.12x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                     |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.93 ms: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.3 ms: 1.08x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 50.9 ms: 1.07x faster                                                    |
| pylint                           | 128 ms                                                   | 120 ms: 1.07x faster                                                     |
| pycparser                        | 497 ms                                                   | 466 ms: 1.07x faster                                                     |
| generators                       | 21.9 ms                                                  | 20.7 ms: 1.06x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.45 us: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.9 ms: 1.05x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.8 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.71 us: 1.03x faster                                                    |
| sphinx                           | 434 ms                                                   | 426 ms: 1.02x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.01x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.6 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 674 ms: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.73 ms: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.14 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.1 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| tomli_loads                      | 957 ms                                                   | 975 ms: 1.02x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.5 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.02x slower                                                    |
| richards                         | 22.4 ms                                                  | 22.9 ms: 1.02x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.0 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 107 us: 1.04x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.05x slower                                                    |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.05x slower                                                     |
| thrift                           | 322 us                                                   | 339 us: 1.05x slower                                                     |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 61.0 ms: 1.06x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.2 ms: 1.06x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.0 ms: 1.08x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.13x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.5 ms: 1.15x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.49 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                    |
| shortest_path                    | 219 ms                                                   | 252 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 55.7 ms: 1.17x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 60.8 ms: 1.18x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.81 ms: 1.22x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.12 ms: 1.25x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 547 us: 1.31x slower                                                     |
| many_optionals                   | 195 us                                                   | 268 us: 1.37x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.5 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.8 ms: 2.89x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (5): typing_runtime_protocols, nqueens, pprint_safe_repr, scimark_sparse_mat_mult, html5lib
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251224-3.15.0a3+-cf6758f-NOGIL/bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.096x faster

# HPT report

- Reliability score: 98.86% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.35x