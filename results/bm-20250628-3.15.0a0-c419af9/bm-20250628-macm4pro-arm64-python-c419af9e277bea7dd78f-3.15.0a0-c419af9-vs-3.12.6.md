# Results vs. 3.12.6

- fork: python
- ref: c419af9e277bea7dd78f
- machine: darwin-arm64
- commit hash: c419af9
- commit date: 2025-06-28
- overall geometric mean: 1.091x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.02x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                   |
| sphinx         | 434 ms                                                   | 414 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 257 ms: 1.93x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 262 ms: 1.83x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 260 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 258 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.54x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.53x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 268 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 271 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.3 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 253 ms: 1.19x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.2 ms: 2.78x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.7 ms: 1.19x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.6 ms: 1.12x faster                                                   |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.8 ms: 1.12x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.2 ms: 1.01x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.77 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 45.9 ms: 1.12x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.8 ms: 1.08x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.6 ms: 1.05x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 65.3 ms: 1.04x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 99.2 us: 1.04x faster                                                   |
| tomli_loads          | 957 ms                                                   | 924 ms: 1.04x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.47 ms: 1.05x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 149 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.71 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.22 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.1 ms: 1.02x slower                                                   |
| mako            | 4.77 ms                                                  | 4.91 ms: 1.03x slower                                                   |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.93 ms: 2.09x faster                                                   |
| mdp                              | 1.09 sec                                                 | 523 ms: 2.09x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 257 ms: 1.93x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 262 ms: 1.83x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 260 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 258 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.54x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.53x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.46x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.41 us: 1.33x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 268 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 271 ms: 1.23x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.19 us: 1.23x faster                                                   |
| go                               | 70.0 ms                                                  | 57.2 ms: 1.22x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 42.2 ns: 1.21x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 45.2 ms: 1.20x faster                                                   |
| float                            | 37.9 ms                                                  | 31.7 ms: 1.19x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 51.4 ms: 1.19x faster                                                   |
| raytrace                         | 145 ms                                                   | 123 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| k_core                           | 1.12 sec                                                 | 957 ms: 1.17x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.16x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.9 ms: 1.16x faster                                                   |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.9 ms: 1.12x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.8 ms: 1.12x faster                                                   |
| nbody                            | 54.2 ms                                                  | 48.6 ms: 1.12x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 63.9 us: 1.11x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.56 ms: 1.11x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.88 ms: 1.11x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 39.4 ms: 1.10x faster                                                   |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.8 ms: 1.08x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.7 ms: 1.08x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.82 ms: 1.08x faster                                                   |
| chaos                            | 28.9 ms                                                  | 27.1 ms: 1.07x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.65 us: 1.06x faster                                                   |
| thrift                           | 322 us                                                   | 305 us: 1.05x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.62 ms: 1.05x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 43.3 ms: 1.05x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.45 us: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 414 ms: 1.05x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.6 ms: 1.05x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 65.3 ms: 1.04x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 99.2 us: 1.04x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 924 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 38.3 ms: 1.02x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 98.2 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 25.2 ms: 1.01x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 51.0 ms: 1.01x faster                                                   |
| richards                         | 22.4 ms                                                  | 22.3 ms: 1.00x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 329 ms: 1.00x slower                                                    |
| shortest_path                    | 219 ms                                                   | 220 ms: 1.00x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| pycparser                        | 497 ms                                                   | 503 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 673 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.4 ms: 1.01x slower                                                   |
| connected_components             | 201 ms                                                   | 204 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.1 ms: 1.02x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.77 ms: 1.02x slower                                                   |
| 2to3                             | 114 ms                                                   | 117 ms: 1.02x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.91 ms: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| bench_thread_pool                | 419 us                                                   | 438 us: 1.05x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.11 ms: 1.05x slower                                                   |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.47 ms: 1.05x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 149 us: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.71 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.22 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.8 ms: 1.13x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 951 us: 1.15x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.05 ms: 1.17x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 253 ms: 1.19x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.1 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.2 ms: 2.78x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (4): sympy_sum, json, fannkuch, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250628-3.15.0a0-c419af9/bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.091x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.15x