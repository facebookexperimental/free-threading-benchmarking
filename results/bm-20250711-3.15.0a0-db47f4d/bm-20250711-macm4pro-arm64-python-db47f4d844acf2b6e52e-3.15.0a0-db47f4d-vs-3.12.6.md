# Results vs. 3.12.6

- fork: python
- ref: db47f4d844acf2b6e52e
- machine: darwin-arm64
- commit hash: db47f4d
- commit date: 2025-07-11
- overall geometric mean: 1.089x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.07 sec: 1.05x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.6 ms: 1.07x slower                                                   |
| sphinx         | 434 ms                                                   | 418 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 254 ms: 1.95x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 257 ms: 1.86x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 257 ms: 1.73x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.54x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 113 ms: 1.53x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 268 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 269 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.8 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.8 ms: 2.79x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.0 ms: 1.22x faster                                                   |
| nbody          | 54.2 ms                                                  | 49.3 ms: 1.10x faster                                                   |
| pidigits       | 161 ms                                                   | 170 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 49.5 ms: 1.10x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 10.1 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.3 ms: 1.16x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.9 ms: 1.11x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.0 ms: 1.08x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.6 ms: 1.04x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.02x faster                                                    |
| tomli_loads          | 957 ms                                                   | 945 ms: 1.01x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.54 ms: 1.07x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 151 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                   |
| python_startup         | 8.01 ms                                                  | 8.79 ms: 1.10x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.2 ms: 1.02x slower                                                   |
| mako            | 4.77 ms                                                  | 4.97 ms: 1.04x slower                                                   |
| django_template | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.05x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.88 ms: 2.10x faster                                                   |
| mdp                              | 1.09 sec                                                 | 523 ms: 2.09x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 254 ms: 1.95x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 257 ms: 1.86x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 257 ms: 1.73x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.54x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 113 ms: 1.53x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                    |
| deepcopy                         | 161 us                                                   | 112 us: 1.44x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.43x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.51 us: 1.31x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 268 ms: 1.27x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.1 ns: 1.24x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 269 ms: 1.24x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.19 us: 1.23x faster                                                   |
| float                            | 37.9 ms                                                  | 31.0 ms: 1.22x faster                                                   |
| go                               | 70.0 ms                                                  | 58.1 ms: 1.20x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.8 ms: 1.20x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 45.6 ms: 1.19x faster                                                   |
| raytrace                         | 145 ms                                                   | 122 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| k_core                           | 1.12 sec                                                 | 955 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.3 ms: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 60.9 ms: 1.11x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 64.0 us: 1.11x faster                                                   |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.56 ms: 1.11x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 49.5 ms: 1.10x faster                                                   |
| nbody                            | 54.2 ms                                                  | 49.3 ms: 1.10x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.3 ms: 1.10x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 39.8 ms: 1.09x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.91 ms: 1.09x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.6 ms: 1.09x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.7 ms: 1.08x faster                                                   |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.0 ms: 1.08x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.07x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.85 ms: 1.07x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.8 ms: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.60 ms: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 307 us: 1.05x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.46 us: 1.04x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.68 us: 1.04x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.6 ms: 1.04x faster                                                   |
| sphinx                           | 434 ms                                                   | 418 ms: 1.04x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                   |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 50.3 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.02x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 945 ms: 1.01x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.4 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 25.2 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| 2to3                             | 114 ms                                                   | 116 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.2 ms: 1.02x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 204 ms: 1.02x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 679 ms: 1.02x slower                                                    |
| pycparser                        | 497 ms                                                   | 509 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 336 ms: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.1 ms: 1.03x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.97 ms: 1.04x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 438 us: 1.05x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.07 sec: 1.05x slower                                                  |
| gc_traversal                     | 2.01 ms                                                  | 2.11 ms: 1.05x slower                                                   |
| pidigits                         | 161 ms                                                   | 170 ms: 1.05x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.1 ms: 1.06x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.54 ms: 1.07x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.6 ms: 1.07x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 151 us: 1.08x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.79 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.6 ms: 1.12x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.03 ms: 1.16x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 965 us: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.8 ms: 1.26x slower                                                   |
| many_optionals                   | 195 us                                                   | 251 us: 1.29x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.8 ms: 2.79x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (5): json, regex_dna, richards, sympy_sum, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.089x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.15x