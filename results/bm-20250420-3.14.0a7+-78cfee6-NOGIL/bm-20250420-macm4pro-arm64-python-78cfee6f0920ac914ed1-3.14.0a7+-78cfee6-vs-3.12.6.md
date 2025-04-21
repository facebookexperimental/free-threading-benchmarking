# Results vs. 3.12.6

- fork: python
- ref: 78cfee6f0920ac914ed1
- machine: darwin-arm64
- commit hash: 78cfee6
- commit date: 2025-04-20
- overall geometric mean: 1.115x faster
- HPT reliability: 99.87%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.04x slower                                                     |
| docutils       | 1.02 sec                                                 | 979 ms: 1.04x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| sphinx         | 434 ms                                                   | 412 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 195 ms: 2.46x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.29x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.0 ms: 2.03x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.88x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 230 ms: 1.47x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.85 ms: 1.38x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 223 ms: 1.05x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 50.0 ms: 1.10x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.1 ms: 2.40x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.39x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.1 ms: 1.40x faster                                                    |
| nbody          | 54.2 ms                                                  | 52.6 ms: 1.03x faster                                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.12x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.8 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.82 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.2 ms: 1.39x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.6 ms: 1.16x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                    |
| tomli_loads          | 957 ms                                                   | 941 ms: 1.02x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 26.3 ms: 1.01x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 102 us: 1.01x faster                                                     |
| pickle_pure_python   | 139 us                                                   | 149 us: 1.07x slower                                                     |
| json_loads           | 10.9 us                                                  | 12.1 us: 1.12x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.98 ms: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.48 ms: 1.18x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.55 ms: 1.32x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.25x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 23.1 ms: 1.06x slower                                                    |
| mako            | 4.77 ms                                                  | 5.44 ms: 1.14x slower                                                    |
| django_template | 13.6 ms                                                  | 16.1 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.11x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 751 us: 2.68x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 195 ms: 2.46x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 8.78 ms: 2.37x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.29x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.0 ms: 2.03x faster                                                    |
| mdp                              | 1.09 sec                                                 | 558 ms: 1.96x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.88x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 443 us: 1.87x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 230 ms: 1.47x faster                                                     |
| float                            | 37.9 ms                                                  | 27.1 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.2 ms: 1.39x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.85 ms: 1.38x faster                                                    |
| deepcopy                         | 161 us                                                   | 122 us: 1.32x faster                                                     |
| generators                       | 21.9 ms                                                  | 17.4 ms: 1.26x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.7 us: 1.25x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 806 ns: 1.20x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.37 us: 1.18x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.91 sec: 1.17x faster                                                   |
| pylint                           | 128 ms                                                   | 110 ms: 1.17x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                    |
| go                               | 70.0 ms                                                  | 60.2 ms: 1.16x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.6 ms: 1.16x faster                                                    |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                     |
| k_core                           | 1.12 sec                                                 | 977 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.12x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.3 ms: 1.12x faster                                                    |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 49.0 ms: 1.11x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.57 ms: 1.10x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.7 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 457 ms: 1.09x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 46.8 ns: 1.09x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.8 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 412 ms: 1.05x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 135 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                     |
| docutils                         | 1.02 sec                                                 | 979 ms: 1.04x faster                                                     |
| chaos                            | 28.9 ms                                                  | 28.0 ms: 1.03x faster                                                    |
| nbody                            | 54.2 ms                                                  | 52.6 ms: 1.03x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.49 us: 1.03x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.82 ms: 1.03x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 941 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.76 us: 1.02x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.3 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 102 us: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.0 ms: 1.01x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 3.06 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 71.7 us: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.82 ms: 1.02x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 59.2 ms: 1.03x slower                                                    |
| sympy_str                        | 104 ms                                                   | 108 ms: 1.03x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.15 ms: 1.03x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 40.2 ms: 1.04x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 53.1 ms: 1.04x slower                                                    |
| json                             | 1.93 ms                                                  | 2.00 ms: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 119 ms: 1.04x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 223 ms: 1.05x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 41.7 ms: 1.05x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 49.1 ms: 1.05x slower                                                    |
| shortest_path                    | 219 ms                                                   | 230 ms: 1.05x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.1 ms: 1.06x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.9 ms: 1.07x slower                                                    |
| fannkuch                         | 176 ms                                                   | 188 ms: 1.07x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 149 us: 1.07x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 354 ms: 1.08x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 27.4 ms: 1.08x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 720 ms: 1.08x slower                                                     |
| connected_components             | 201 ms                                                   | 218 ms: 1.09x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.66 ms: 1.09x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 50.0 ms: 1.10x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.11x slower                                                     |
| json_loads                       | 10.9 us                                                  | 12.1 us: 1.12x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.44 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.0 ms: 1.15x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.98 ms: 1.17x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.1 ms: 1.18x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.48 ms: 1.18x slower                                                    |
| many_optionals                   | 195 us                                                   | 241 us: 1.23x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.28 ms: 1.26x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.55 ms: 1.32x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 566 us: 1.35x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.0 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.1 ms: 2.40x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (1): regex_dna
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250420-3.14.0a7+-78cfee6-NOGIL/bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.115x faster

# HPT report

- Reliability score: 99.87% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.22x