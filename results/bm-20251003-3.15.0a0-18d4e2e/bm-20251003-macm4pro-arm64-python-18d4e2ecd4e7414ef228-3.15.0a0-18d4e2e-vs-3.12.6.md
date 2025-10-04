# Results vs. 3.12.6

- fork: python
- ref: 18d4e2ecd4e7414ef228
- machine: darwin-arm64
- commit hash: 18d4e2e
- commit date: 2025-10-03
- overall geometric mean: 1.077x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.07 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 25.0 ms: 1.09x slower                                                   |
| sphinx         | 434 ms                                                   | 419 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 257 ms: 1.93x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 257 ms: 1.87x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 258 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.59x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.53x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.53x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 152 ms: 1.47x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.18x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.0 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 90.0 ms: 2.80x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.8 ms: 1.19x faster                                                   |
| nbody          | 54.2 ms                                                  | 51.5 ms: 1.05x faster                                                   |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 50.5 ms: 1.08x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.1 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.5 ms: 1.07x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 63.8 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.9 ms: 1.03x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 104 us: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.02x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 151 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.79 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.6 ms: 1.04x slower                                                   |
| mako            | 4.77 ms                                                  | 5.11 ms: 1.07x slower                                                   |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.06x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 555 ms: 1.97x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 257 ms: 1.93x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 257 ms: 1.87x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 258 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.59x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.53x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.53x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 152 ms: 1.47x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                   |
| deepcopy                         | 161 us                                                   | 113 us: 1.43x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.74 us: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.19 us: 1.23x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 44.7 ms: 1.22x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.9 ns: 1.22x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.1 ms: 1.21x faster                                                   |
| go                               | 70.0 ms                                                  | 58.2 ms: 1.20x faster                                                   |
| float                            | 37.9 ms                                                  | 31.8 ms: 1.19x faster                                                   |
| raytrace                         | 145 ms                                                   | 122 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                   |
| k_core                           | 1.12 sec                                                 | 967 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 53.1 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.4 ms: 1.13x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.85 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.01 sec: 1.12x faster                                                  |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.5 ms: 1.10x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 64.6 us: 1.10x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.58 ms: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 50.5 ms: 1.08x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.40 us: 1.07x faster                                                   |
| pyflate                          | 216 ms                                                   | 203 ms: 1.07x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.63 us: 1.07x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.5 ms: 1.07x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 63.8 ms: 1.06x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 43.0 ms: 1.06x faster                                                   |
| chaos                            | 28.9 ms                                                  | 27.3 ms: 1.06x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.58 ms: 1.06x faster                                                   |
| nbody                            | 54.2 ms                                                  | 51.5 ms: 1.05x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.8 ms: 1.05x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.90 ms: 1.05x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.8 ms: 1.04x faster                                                   |
| sphinx                           | 434 ms                                                   | 419 ms: 1.03x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.9 ms: 1.03x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.9 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 98.1 ms: 1.02x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 25.1 ms: 1.01x faster                                                   |
| richards                         | 22.4 ms                                                  | 22.2 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 961 ns: 1.01x faster                                                    |
| thrift                           | 322 us                                                   | 320 us: 1.01x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 57.3 ms: 1.00x faster                                                   |
| bench_thread_pool                | 419 us                                                   | 422 us: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 104 us: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| connected_components             | 201 ms                                                   | 203 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.02x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 676 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 335 ms: 1.02x slower                                                    |
| pycparser                        | 497 ms                                                   | 511 ms: 1.03x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 173 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.6 ms: 1.04x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.07 sec: 1.04x slower                                                  |
| gc_traversal                     | 2.01 ms                                                  | 2.11 ms: 1.05x slower                                                   |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 50.9 ms: 1.07x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 42.4 ms: 1.07x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.11 ms: 1.07x slower                                                   |
| fannkuch                         | 176 ms                                                   | 189 ms: 1.08x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 151 us: 1.09x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 25.0 ms: 1.09x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.79 ms: 1.10x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.90 ms: 1.11x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 940 us: 1.13x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.2 ms: 1.24x slower                                                   |
| many_optionals                   | 195 us                                                   | 332 us: 1.70x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 90.0 ms: 2.80x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (3): genshi_text, shortest_path, tomli_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251003-3.15.0a0-18d4e2e/bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.077x faster

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.14x