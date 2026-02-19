# Results vs. 3.12.6

- fork: python
- ref: 0bbdb4e897ae909af39c
- machine: darwin-arm64
- commit hash: 0bbdb4e
- commit date: 2026-02-18
- overall geometric mean: 1.091x faster
- HPT reliability: 99.84%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.01x faster                                                   |
| sphinx         | 434 ms                                                   | 424 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 236 ms: 2.04x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 248 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 247 ms: 1.86x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 243 ms: 1.83x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.47x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.16x faster                                                     |
| async_generators                 | 206 ms                                                   | 187 ms: 1.10x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.02x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.7 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.7 ms: 2.89x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.4 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.8 ms: 1.07x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.2 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.2 ms: 1.11x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.88 ms: 1.10x faster                                                    |
| tomli_loads          | 957 ms                                                   | 883 ms: 1.08x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.06x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.0 ms: 1.25x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.28 ms: 1.28x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.26x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.8 ms: 1.05x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                    |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                    |
| mako            | 4.77 ms                                                  | 5.53 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.14 ms: 5.02x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 799 us: 2.51x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 236 ms: 2.04x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 248 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 247 ms: 1.86x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 243 ms: 1.83x faster                                                     |
| mdp                              | 1.09 sec                                                 | 612 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 507 us: 1.64x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                     |
| deepcopy                         | 161 us                                                   | 107 us: 1.51x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.47x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.45x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                    |
| float                            | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.25x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 789 ns: 1.23x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.27 us: 1.19x faster                                                    |
| go                               | 70.0 ms                                                  | 59.9 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.16x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 43.9 ns: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 990 ms: 1.13x faster                                                     |
| raytrace                         | 145 ms                                                   | 128 ms: 1.13x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 61.2 ms: 1.11x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.1 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                     |
| async_generators                 | 206 ms                                                   | 187 ms: 1.10x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.88 ms: 1.10x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 883 ms: 1.08x faster                                                     |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 50.8 ms: 1.07x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.40 us: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 466 ms: 1.07x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 51.3 ms: 1.06x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.2 ms: 1.05x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.68 us: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                    |
| generators                       | 21.9 ms                                                  | 21.1 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.8 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.02x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 42.5 ms: 1.02x faster                                                    |
| sphinx                           | 434 ms                                                   | 424 ms: 1.02x faster                                                     |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 322 ms: 1.02x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.01x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 663 ms: 1.00x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.5 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.19 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 72.7 us: 1.02x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.7 ms: 1.03x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.1 ms: 1.03x slower                                                    |
| thrift                           | 322 us                                                   | 333 us: 1.03x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.15 ms: 1.04x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.3 ms: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.8 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.06x slower                                                     |
| nbody                            | 54.2 ms                                                  | 57.4 ms: 1.06x slower                                                    |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                     |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 61.5 ms: 1.07x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 57.4 ms: 1.12x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.13x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 44.2 ms: 1.14x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.53 ms: 1.16x slower                                                    |
| shortest_path                    | 219 ms                                                   | 254 ms: 1.16x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.03 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 55.4 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 47.0 ms: 1.18x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 10.0 ms: 1.25x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.28 ms: 1.28x slower                                                    |
| many_optionals                   | 195 us                                                   | 266 us: 1.36x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 575 us: 1.37x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.9 ms: 1.45x slower                                                    |
| connected_components             | 201 ms                                                   | 302 ms: 1.51x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.7 ms: 2.89x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (2): html5lib, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260218-3.15.0a6+-0bbdb4e-NOGIL/bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.091x faster

# HPT report

- Reliability score: 99.84% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.37x