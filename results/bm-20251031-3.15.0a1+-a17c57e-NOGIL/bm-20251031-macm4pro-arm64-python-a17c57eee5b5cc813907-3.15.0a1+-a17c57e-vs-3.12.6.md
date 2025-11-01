# Results vs. 3.12.6

- fork: python
- ref: a17c57eee5b5cc813907
- machine: darwin-arm64
- commit hash: a17c57e
- commit date: 2025-10-31
- overall geometric mean: 1.071x faster
- HPT reliability: 93.12%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| sphinx         | 434 ms                                                   | 423 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.40x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 200 ms: 2.39x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.27x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 213 ms: 2.15x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 88.0 ms: 1.96x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.84x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| async_generators                 | 206 ms                                                   | 180 ms: 1.14x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 49.7 ms: 1.09x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.9 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.0 ms: 1.26x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 56.9 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.0 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.35 ms: 1.03x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 54.4 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.9 ms: 1.26x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.1 ms: 1.15x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.09 ms: 1.04x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 38.3 ms: 1.02x faster                                                    |
| tomli_loads          | 957 ms                                                   | 982 ms: 1.03x slower                                                     |
| xml_etree_process    | 26.7 ms                                                  | 27.8 ms: 1.04x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 113 us: 1.10x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 157 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.72 ms: 1.21x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.07 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.8 ms: 1.13x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 24.7 ms: 1.13x slower                                                    |
| mako            | 4.77 ms                                                  | 5.88 ms: 1.23x slower                                                    |
| django_template | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.18x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 771 us: 2.61x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.40x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 200 ms: 2.39x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.27x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 213 ms: 2.15x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 88.0 ms: 1.96x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.84x faster                                                     |
| mdp                              | 1.09 sec                                                 | 612 ms: 1.78x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 478 us: 1.74x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.3 us: 1.38x faster                                                    |
| deepcopy                         | 161 us                                                   | 118 us: 1.36x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| float                            | 37.9 ms                                                  | 30.0 ms: 1.26x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.9 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 835 ns: 1.16x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.27 us: 1.15x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.55 us: 1.15x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.1 ms: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 997 ms: 1.12x faster                                                     |
| go                               | 70.0 ms                                                  | 62.9 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.03 sec: 1.11x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.3 ms: 1.10x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 46.2 ns: 1.10x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.3 ms: 1.10x faster                                                    |
| raytrace                         | 145 ms                                                   | 133 ms: 1.09x faster                                                     |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 19.2 ms: 1.08x faster                                                    |
| pyflate                          | 216 ms                                                   | 201 ms: 1.07x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 135 ms: 1.05x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 52.0 ms: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.05x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.09 ms: 1.04x faster                                                    |
| pycparser                        | 497 ms                                                   | 479 ms: 1.04x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 96.0 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.35 ms: 1.03x faster                                                    |
| sphinx                           | 434 ms                                                   | 423 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 38.3 ms: 1.02x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 54.4 ms: 1.00x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.08 ms: 1.01x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.84 us: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| chaos                            | 28.9 ms                                                  | 29.4 ms: 1.02x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 982 ms: 1.03x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 44.9 ms: 1.03x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.8 ms: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                    |
| json                             | 1.93 ms                                                  | 2.01 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.9 ms: 1.05x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 74.6 us: 1.05x slower                                                    |
| fannkuch                         | 176 ms                                                   | 184 ms: 1.05x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.19 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| thrift                           | 322 us                                                   | 342 us: 1.06x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.2 ms: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.2 ms: 1.06x slower                                                    |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                     |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| sympy_str                        | 104 ms                                                   | 113 ms: 1.08x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 49.7 ms: 1.09x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 43.4 ms: 1.09x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.6 ms: 1.10x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 361 ms: 1.10x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 113 us: 1.10x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 28.0 ms: 1.10x slower                                                    |
| connected_components             | 201 ms                                                   | 222 ms: 1.11x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 736 ms: 1.11x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 43.4 ms: 1.12x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.8 ms: 1.13x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 157 us: 1.13x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 24.7 ms: 1.13x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 193 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 56.6 ms: 1.19x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.10 ms: 1.19x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.72 ms: 1.21x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.88 ms: 1.23x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.07 ms: 1.24x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 64.3 ms: 1.25x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 539 us: 1.29x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.2 ms: 1.50x slower                                                    |
| many_optionals                   | 195 us                                                   | 384 us: 1.97x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.9 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                             |

Benchmark hidden because not significant (3): async_tree_eager_memoization_tg, logging_simple, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251031-3.15.0a1+-a17c57e-NOGIL/bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 93.12% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.34x