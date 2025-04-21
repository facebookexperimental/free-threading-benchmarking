# Results vs. 3.12.6

- fork: python
- ref: 78cfee6f0920ac914ed1
- machine: darwin-arm64
- commit hash: 78cfee6
- commit date: 2025-04-20
- overall geometric mean: 1.099x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| sphinx         | 434 ms                                                   | 411 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.81x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.65x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                     |
| async_generators                 | 206 ms                                                   | 171 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 43.0 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.0 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.8 ms: 1.27x faster                                                    |
| nbody          | 54.2 ms                                                  | 49.1 ms: 1.11x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                    | 1.12x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 48.6 ms: 1.12x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 98.6 ms: 1.01x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| tomli_loads          | 957 ms                                                   | 924 ms: 1.04x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 25.9 ms: 1.03x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                     |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.02 ms: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.95 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.71 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.7 ms: 1.01x faster                                                    |
| mako            | 4.77 ms                                                  | 4.90 ms: 1.03x slower                                                    |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.13x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.72 ms: 2.38x faster                                                    |
| mdp                              | 1.09 sec                                                 | 522 ms: 2.09x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.81x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.65x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                     |
| deepcopy                         | 161 us                                                   | 108 us: 1.49x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.43x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.12 us: 1.30x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.62 us: 1.29x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| float                            | 37.9 ms                                                  | 29.8 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.7 ns: 1.25x faster                                                    |
| async_generators                 | 206 ms                                                   | 171 ms: 1.20x faster                                                     |
| go                               | 70.0 ms                                                  | 58.4 ms: 1.20x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.9 ms: 1.19x faster                                                    |
| raytrace                         | 145 ms                                                   | 122 ms: 1.19x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.5 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| k_core                           | 1.12 sec                                                 | 945 ms: 1.18x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 51.6 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 47.2 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.6 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.3 ms: 1.11x faster                                                    |
| nbody                            | 54.2 ms                                                  | 49.1 ms: 1.11x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.56 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.8 ms: 1.08x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 66.0 us: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.48 ms: 1.07x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.1 ms: 1.07x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 133 ms: 1.07x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.95 ms: 1.07x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.86 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.0 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.44 us: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 411 ms: 1.05x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.68 us: 1.05x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.8 ms: 1.04x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 924 ms: 1.04x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 45.2 ms: 1.04x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.9 ms: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.8 ms: 1.03x faster                                                    |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 38.0 ms: 1.02x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 50.2 ms: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 98.6 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.7 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                     |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                     |
| sqlite_synth                     | 967 ns                                                   | 975 ns: 1.01x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 25.6 ms: 1.01x slower                                                    |
| connected_components             | 201 ms                                                   | 203 ms: 1.01x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 40.2 ms: 1.01x slower                                                    |
| richards                         | 22.4 ms                                                  | 22.7 ms: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 677 ms: 1.02x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 335 ms: 1.02x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.90 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.0 ms: 1.03x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.39 ms: 1.04x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 874 us: 1.05x slower                                                     |
| fannkuch                         | 176 ms                                                   | 185 ms: 1.05x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 443 us: 1.06x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.95 ms: 1.12x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.13x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.71 ms: 1.18x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.02 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                     |
| many_optionals                   | 195 us                                                   | 233 us: 1.19x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.0 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (4): pycparser, gc_traversal, shortest_path, json
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250420-3.14.0a7+-78cfee6/bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.099x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.13x