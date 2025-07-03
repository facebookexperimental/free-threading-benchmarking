# Results vs. 3.12.6

- fork: python
- ref: 7afe1adb0089d0f2df2a
- machine: darwin-arm64
- commit hash: 7afe1ad
- commit date: 2025-07-02
- overall geometric mean: 1.087x faster
- HPT reliability: 91.75%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 419 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 201 ms: 2.39x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 208 ms: 2.39x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 197 ms: 2.27x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 212 ms: 2.16x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 88.0 ms: 1.96x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.74x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 50.5 ms: 1.11x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.3 ms: 2.47x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                   |
| nbody          | 54.2 ms                                                  | 55.2 ms: 1.02x slower                                                   |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.29 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.1 ms: 1.03x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 101 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 36.6 ms: 1.41x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.0 ms: 1.19x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.9 ms: 1.00x slower                                                   |
| tomli_loads          | 957 ms                                                   | 1.00 sec: 1.05x slower                                                  |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.55 ms: 1.07x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.08x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.84 ms: 1.23x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.10 ms: 1.24x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.24x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.08x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 24.0 ms: 1.10x slower                                                   |
| django_template | 13.6 ms                                                  | 16.4 ms: 1.21x slower                                                   |
| mako            | 4.77 ms                                                  | 5.77 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 805 us: 2.49x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 201 ms: 2.39x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 208 ms: 2.39x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 197 ms: 2.27x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 212 ms: 2.16x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.84 ms: 2.11x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 88.0 ms: 1.96x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.85x faster                                                    |
| mdp                              | 1.09 sec                                                 | 589 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.74x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 502 us: 1.65x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.44x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.6 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| deepcopy                         | 161 us                                                   | 122 us: 1.33x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.0 us: 1.31x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                   |
| float                            | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.08 us: 1.22x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 57.0 ms: 1.19x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 823 ns: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.4 ns: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| generators                       | 21.9 ms                                                  | 19.4 ms: 1.13x faster                                                   |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| go                               | 70.0 ms                                                  | 62.2 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.00 sec: 1.12x faster                                                  |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.11x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.2 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.5 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 199 ms: 1.08x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                   |
| pylint                           | 128 ms                                                   | 120 ms: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                   |
| pycparser                        | 497 ms                                                   | 474 ms: 1.05x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.8 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 419 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.29 ms: 1.03x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 42.2 ms: 1.03x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 53.1 ms: 1.03x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.9 ms: 1.00x slower                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.07 ms: 1.01x slower                                                   |
| regex_dna                        | 99.6 ms                                                  | 101 ms: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.4 ms: 1.02x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.62 us: 1.02x slower                                                   |
| nbody                            | 54.2 ms                                                  | 55.2 ms: 1.02x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.10 ms: 1.02x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.2 us: 1.03x slower                                                   |
| fannkuch                         | 176 ms                                                   | 182 ms: 1.04x slower                                                    |
| json                             | 1.93 ms                                                  | 2.01 ms: 1.04x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.92 us: 1.04x slower                                                   |
| scimark_fft                      | 142 ms                                                   | 148 ms: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 337 us: 1.05x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.7 ms: 1.05x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 1.00 sec: 1.05x slower                                                  |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 348 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.55 ms: 1.07x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.5 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 712 ms: 1.07x slower                                                    |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.23 ms: 1.08x slower                                                   |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.2 ms: 1.08x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.08x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.08x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.1 ms: 1.08x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.6 ms: 1.09x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 24.0 ms: 1.10x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 50.5 ms: 1.11x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 56.9 ms: 1.11x slower                                                   |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 191 ms: 1.14x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.4 ms: 1.14x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 56.6 ms: 1.19x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.4 ms: 1.21x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.77 ms: 1.21x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.84 ms: 1.23x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.10 ms: 1.24x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.26 ms: 1.25x slower                                                   |
| many_optionals                   | 195 us                                                   | 257 us: 1.31x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 581 us: 1.39x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.1 ms: 1.49x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.3 ms: 2.47x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.087x faster

# HPT report

- Reliability score: 91.75% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x