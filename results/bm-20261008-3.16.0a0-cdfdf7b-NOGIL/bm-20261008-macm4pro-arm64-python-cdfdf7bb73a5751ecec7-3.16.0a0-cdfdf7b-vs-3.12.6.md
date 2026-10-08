# Results vs. 3.12.6

- fork: python
- ref: cdfdf7bb73a5751ecec7
- machine: darwin-arm64
- commit hash: cdfdf7b
- commit date: 2026-10-08
- overall geometric mean: 1.056x faster
- HPT reliability: 87.14%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 130 ms: 1.14x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 443 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 295 ms: 1.68x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 294 ms: 1.63x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 293 ms: 1.52x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 307 ms: 1.50x faster                                                    |
| async_generators                 | 206 ms                                                   | 161 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 180 ms: 1.28x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 143 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 139 ms: 1.24x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 185 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 293 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 299 ms: 1.11x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 12.7 ms: 1.07x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 125 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 233 ms: 1.01x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 50.1 ms: 1.10x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 274 ms: 1.29x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 163 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 113 ms: 3.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 33.0 ms: 1.15x faster                                                   |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| nbody          | 54.2 ms                                                  | 59.0 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.34 ms: 1.24x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 91.2 ms: 1.09x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 64.3 ms: 1.18x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.5 ms: 1.24x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.2 ms: 1.15x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.75 ms: 1.14x faster                                                   |
| tomli_loads          | 957 ms                                                   | 891 ms: 1.07x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 38.7 ms: 1.00x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 155 us: 1.11x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 29.8 ms: 1.11x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.33 ms: 1.29x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.27x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.77 ms: 1.21x slower                                                   |
| django_template | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.23x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.36 ms: 4.77x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 777 us: 2.59x faster                                                    |
| pylint                           | 128 ms                                                   | 53.6 ms: 2.39x faster                                                   |
| mdp                              | 1.09 sec                                                 | 599 ms: 1.82x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 492 us: 1.69x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 295 ms: 1.68x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 294 ms: 1.63x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 293 ms: 1.52x faster                                                    |
| deepcopy                         | 161 us                                                   | 107 us: 1.50x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 307 ms: 1.50x faster                                                    |
| async_generators                 | 206 ms                                                   | 161 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 180 ms: 1.28x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.6 us: 1.26x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 143 ms: 1.25x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.5 ms: 1.24x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.34 ms: 1.24x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 139 ms: 1.24x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 57.7 us: 1.23x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 787 ns: 1.23x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 185 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 293 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.16x faster                                                  |
| float                            | 37.9 ms                                                  | 33.0 ms: 1.15x faster                                                   |
| go                               | 70.0 ms                                                  | 60.9 ms: 1.15x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 59.2 ms: 1.15x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.58 us: 1.15x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.75 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 299 ms: 1.11x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.00 sec: 1.11x faster                                                  |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 48.9 ms: 1.11x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.3 ms: 1.10x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 91.2 ms: 1.09x faster                                                   |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 891 ms: 1.07x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 12.7 ms: 1.07x faster                                                   |
| raytrace                         | 145 ms                                                   | 136 ms: 1.06x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 125 ms: 1.05x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 58.1 ms: 1.05x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 48.5 ns: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.47 us: 1.04x faster                                                   |
| pycparser                        | 497 ms                                                   | 479 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.73 us: 1.03x faster                                                   |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 38.7 ms: 1.00x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 43.3 ms: 1.00x faster                                                   |
| chaos                            | 28.9 ms                                                  | 28.8 ms: 1.00x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 233 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.18 ms: 1.02x slower                                                   |
| sphinx                           | 434 ms                                                   | 443 ms: 1.02x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.7 ms: 1.05x slower                                                   |
| deltablue                        | 1.73 ms                                                  | 1.81 ms: 1.05x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.20 ms: 1.06x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.3 ms: 1.07x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 41.6 ms: 1.07x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.26 ms: 1.07x slower                                                   |
| generators                       | 21.9 ms                                                  | 23.5 ms: 1.07x slower                                                   |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.07x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 354 ms: 1.08x slower                                                    |
| nbody                            | 54.2 ms                                                  | 59.0 ms: 1.09x slower                                                   |
| thrift                           | 322 us                                                   | 351 us: 1.09x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 43.7 ms: 1.10x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.9 ms: 1.10x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 50.1 ms: 1.10x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.7 ms: 1.10x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 155 us: 1.11x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 740 ms: 1.11x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 29.8 ms: 1.11x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                    |
| shortest_path                    | 219 ms                                                   | 249 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.2 ms: 1.14x slower                                                   |
| 2to3                             | 114 ms                                                   | 130 ms: 1.14x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 64.3 ms: 1.18x slower                                                   |
| connected_components             | 201 ms                                                   | 240 ms: 1.20x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.15 ms: 1.21x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.77 ms: 1.21x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 63.2 ms: 1.23x slower                                                   |
| django_template                  | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.33 ms: 1.29x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 274 ms: 1.29x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 568 us: 1.36x slower                                                    |
| many_optionals                   | 195 us                                                   | 269 us: 1.38x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 163 ms: 1.45x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.5 ms: 1.51x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 113 ms: 3.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (2): fannkuch, json_loads
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.056x faster

# HPT report

- Reliability score: 87.14% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.30x