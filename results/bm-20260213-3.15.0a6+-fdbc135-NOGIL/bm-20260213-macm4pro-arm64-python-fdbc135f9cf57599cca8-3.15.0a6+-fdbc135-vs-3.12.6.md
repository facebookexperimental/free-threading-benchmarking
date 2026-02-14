# Results vs. 3.12.6

- fork: python
- ref: fdbc135f9cf57599cca8
- machine: darwin-arm64
- commit hash: fdbc135
- commit date: 2026-02-13
- overall geometric mean: 1.093x faster
- HPT reliability: 99.89%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                   |
| sphinx         | 434 ms                                                   | 423 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.02x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 238 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.85x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 242 ms: 1.84x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.61x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.48x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.30x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 269 ms: 1.24x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 189 ms: 1.09x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.2 ms: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.1 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.0 ms: 1.30x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.6 ms: 1.08x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.14 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.3 ms: 1.15x faster                                                    |
| tomli_loads          | 957 ms                                                   | 871 ms: 1.10x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.95 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.2 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.05x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.83 ms: 1.23x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.13 ms: 1.25x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.24x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.7 ms: 1.04x slower                                                    |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 12.3 ms: 1.17x slower                                                    |
| mako            | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.15 ms: 5.00x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 805 us: 2.49x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.02x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 238 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.85x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 242 ms: 1.84x faster                                                     |
| mdp                              | 1.09 sec                                                 | 610 ms: 1.79x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 507 us: 1.64x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.61x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| deepcopy                         | 161 us                                                   | 106 us: 1.52x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.48x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.30x faster                                                     |
| float                            | 37.9 ms                                                  | 29.0 ms: 1.30x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 269 ms: 1.24x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 789 ns: 1.23x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.29 us: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                     |
| go                               | 70.0 ms                                                  | 59.7 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.1 ns: 1.15x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.3 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 986 ms: 1.13x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.13x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.2 ms: 1.12x faster                                                    |
| raytrace                         | 145 ms                                                   | 129 ms: 1.12x faster                                                     |
| pyflate                          | 216 ms                                                   | 193 ms: 1.12x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.04 sec: 1.10x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 871 ms: 1.10x faster                                                     |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                     |
| async_generators                 | 206 ms                                                   | 189 ms: 1.09x faster                                                     |
| pycparser                        | 497 ms                                                   | 461 ms: 1.08x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 50.6 ms: 1.08x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.95 ms: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.8 ms: 1.07x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.41 us: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.67 us: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.14 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.2 ms: 1.05x faster                                                    |
| generators                       | 21.9 ms                                                  | 21.1 ms: 1.04x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.0 ms: 1.03x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 42.4 ms: 1.03x faster                                                    |
| sphinx                           | 434 ms                                                   | 423 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 325 ms: 1.01x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 661 ms: 1.00x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.4 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.10 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.3 us: 1.02x slower                                                    |
| richards                         | 22.4 ms                                                  | 22.9 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.02x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.2 ms: 1.03x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.2 ms: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.15 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.16 ms: 1.04x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.7 ms: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 336 us: 1.04x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.05x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.8 ms: 1.06x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                     |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                     |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 43.3 ms: 1.11x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 58.1 ms: 1.13x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 192 ms: 1.15x slower                                                     |
| shortest_path                    | 219 ms                                                   | 252 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 55.2 ms: 1.16x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 12.3 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 47.1 ms: 1.19x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.83 ms: 1.23x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.13 ms: 1.25x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 551 us: 1.32x slower                                                     |
| many_optionals                   | 195 us                                                   | 270 us: 1.38x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.7 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.1 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (3): html5lib, dask, fannkuch
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260213-3.15.0a6+-fdbc135-NOGIL/bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.093x faster

# HPT report

- Reliability score: 99.89% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.36x