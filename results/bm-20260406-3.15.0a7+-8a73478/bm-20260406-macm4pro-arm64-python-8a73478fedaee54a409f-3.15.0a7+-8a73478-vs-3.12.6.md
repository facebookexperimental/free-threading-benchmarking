# Results vs. 3.12.6

- fork: python
- ref: 8a73478fedaee54a409f
- machine: darwin-arm64
- commit hash: 8a73478
- commit date: 2026-04-06
- overall geometric mean: 1.174x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| docutils       | 1.02 sec                                                 | 993 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 21.0 ms: 1.10x faster                                                    |
| sphinx         | 434 ms                                                   | 390 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 221 ms: 2.24x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 224 ms: 2.14x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 218 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 230 ms: 2.00x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.2 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.70x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.63x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.98 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.26x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 39.8 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.11x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.5 ms: 2.51x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.5 ms: 1.43x faster                                                    |
| nbody          | 54.2 ms                                                  | 43.3 ms: 1.25x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.22x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.7 ms: 1.20x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                    |
| tomli_loads          | 957 ms                                                   | 802 ms: 1.19x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.72 ms: 1.15x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.2 ms: 1.13x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 98.4 us: 1.05x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 137 us: 1.02x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.12x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.67 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.48 ms: 1.11x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.7 ms: 1.05x faster                                                    |
| mako            | 4.77 ms                                                  | 4.72 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.98 ms: 5.22x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 221 ms: 2.24x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 224 ms: 2.14x faster                                                     |
| mdp                              | 1.09 sec                                                 | 526 ms: 2.07x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 218 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 230 ms: 2.00x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.2 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.70x faster                                                     |
| deepcopy                         | 161 us                                                   | 97.0 us: 1.67x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.63x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.57x faster                                                    |
| float                            | 37.9 ms                                                  | 26.5 ms: 1.43x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.08 us: 1.39x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.05 us: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.98 ms: 1.36x faster                                                    |
| go                               | 70.0 ms                                                  | 51.7 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 41.5 ms: 1.31x faster                                                    |
| raytrace                         | 145 ms                                                   | 112 ms: 1.30x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.26x faster                                                     |
| nbody                            | 54.2 ms                                                  | 43.3 ms: 1.25x faster                                                    |
| k_core                           | 1.12 sec                                                 | 896 ms: 1.25x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.3 ms: 1.24x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 115 ms: 1.24x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 41.5 ns: 1.23x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.15 us: 1.20x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.3 ms: 1.20x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 45.7 ms: 1.20x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.35 us: 1.19x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 802 ms: 1.19x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                    |
| pyflate                          | 216 ms                                                   | 181 ms: 1.19x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.1 ms: 1.19x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.4 ms: 1.18x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 36.8 ms: 1.18x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.91 sec: 1.17x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 44.4 ms: 1.16x faster                                                    |
| pylint                           | 128 ms                                                   | 112 ms: 1.15x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 39.8 ms: 1.15x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.72 ms: 1.15x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.81 ms: 1.14x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.2 ms: 1.13x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.3 us: 1.12x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.72 ms: 1.12x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                    |
| sphinx                           | 434 ms                                                   | 390 ms: 1.11x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 22.9 ms: 1.11x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.48 ms: 1.11x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.3 ms: 1.11x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.0 ms: 1.10x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.35 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 457 ms: 1.09x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 630 ms: 1.06x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 54.6 ms: 1.05x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 20.7 ms: 1.05x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 313 ms: 1.05x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 98.4 us: 1.05x faster                                                    |
| fannkuch                         | 176 ms                                                   | 168 ms: 1.05x faster                                                     |
| sympy_str                        | 104 ms                                                   | 99.7 ms: 1.05x faster                                                    |
| json                             | 1.93 ms                                                  | 1.86 ms: 1.04x faster                                                    |
| thrift                           | 322 us                                                   | 311 us: 1.04x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 993 ms: 1.03x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 942 ns: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 38.0 ms: 1.02x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 137 us: 1.02x faster                                                     |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.72 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 425 us: 1.01x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                     |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 48.6 ms: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.67 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.83 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.11x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 931 us: 1.12x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 44.7 ms: 1.13x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.2 ms: 1.20x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.42 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 248 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.5 ms: 2.51x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.17x faster                                                             |

Benchmark hidden because not significant (1): regex_v8
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260406-3.15.0a7+-8a73478/bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.174x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.24x