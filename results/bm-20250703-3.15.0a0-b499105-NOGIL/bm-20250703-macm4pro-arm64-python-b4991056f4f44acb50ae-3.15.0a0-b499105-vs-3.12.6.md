# Results vs. 3.12.6

- fork: python
- ref: b4991056f4f44acb50ae
- machine: darwin-arm64
- commit hash: b499105
- commit date: 2025-07-03
- overall geometric mean: 1.098x faster
- HPT reliability: 97.73%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.29x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.1 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.29x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.09x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.5 ms: 1.09x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.1 ms: 2.46x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| nbody          | 54.2 ms                                                  | 54.9 ms: 1.01x slower                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.2 ms: 1.05x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.0 ms: 1.36x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.4 ms: 1.16x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.6 ms: 1.00x faster                                                   |
| tomli_loads          | 957 ms                                                   | 971 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.64 ms: 1.09x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.62 ms: 1.20x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.99 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.4 ms: 1.07x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| mako            | 4.77 ms                                                  | 5.60 ms: 1.17x slower                                                   |
| django_template | 13.6 ms                                                  | 16.0 ms: 1.18x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 789 us: 2.55x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.29x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.18x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.80 ms: 2.12x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 87.1 ms: 1.98x faster                                                   |
| mdp                              | 1.09 sec                                                 | 574 ms: 1.90x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 491 us: 1.69x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.0 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.35x faster                                                    |
| deepcopy                         | 161 us                                                   | 120 us: 1.35x faster                                                    |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 14.0 us: 1.31x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.29x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.88 us: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 817 ns: 1.18x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.4 ms: 1.16x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| go                               | 70.0 ms                                                  | 61.0 ms: 1.15x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.3 ms: 1.14x faster                                                   |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 991 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.13x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 45.5 ns: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.1 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 131 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.07x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 471 ms: 1.06x faster                                                    |
| sphinx                           | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.8 ms: 1.05x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 52.2 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 42.1 ms: 1.03x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 139 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                  |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 3.02 ms: 1.01x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 26.6 ms: 1.00x faster                                                   |
| dask                             | 528 ms                                                   | 530 ms: 1.00x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.06 ms: 1.00x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.59 us: 1.01x slower                                                   |
| nbody                            | 54.2 ms                                                  | 54.9 ms: 1.01x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 971 ms: 1.01x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.4 ms: 1.02x slower                                                   |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.9 us: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 331 us: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.90 us: 1.03x slower                                                   |
| json                             | 1.93 ms                                                  | 2.02 ms: 1.05x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.5 ms: 1.05x slower                                                   |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.9 ms: 1.05x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 346 ms: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.9 ms: 1.06x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.9 ms: 1.06x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 705 ms: 1.06x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.22 ms: 1.07x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.4 ms: 1.07x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.0 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.09x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.5 ms: 1.09x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 55.9 ms: 1.09x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.64 ms: 1.09x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                    |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.2 ms: 1.14x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 54.5 ms: 1.14x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.60 ms: 1.17x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.0 ms: 1.18x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.62 ms: 1.20x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.99 ms: 1.23x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.22 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 257 us: 1.32x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 584 us: 1.39x slower                                                    |
| coverage                         | 26.9 ms                                                  | 41.0 ms: 1.53x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.1 ms: 2.46x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250703-3.15.0a0-b499105-NOGIL/bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.098x faster

# HPT report

- Reliability score: 97.73% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x