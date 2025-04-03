# Results vs. 3.12.6

- fork: python
- ref: ca1bedc9a4da523f4d1f
- machine: darwin-arm64
- commit hash: ca1bedc
- commit date: 2025-03-14
- overall geometric mean: 1.047x faster
- HPT reliability: 53.78%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 126 ms: 1.10x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 24.5 ms: 1.07x slower                                                    |
| sphinx         | 434 ms                                                   | 426 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 205 ms: 2.35x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 216 ms: 2.30x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 204 ms: 2.18x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 220 ms: 2.09x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 90.8 ms: 1.90x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 131 ms: 1.77x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 107 ms: 1.66x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.61x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 248 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 118 ms: 1.12x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 230 ms: 1.08x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 52.8 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.5 ms: 2.54x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.32x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.4 ms: 1.17x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| nbody          | 54.2 ms                                                  | 63.3 ms: 1.17x slower                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.51 ms: 1.10x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 56.0 ms: 1.03x slower                                                    |
| regex_dna      | 99.6 ms                                                  | 102 ms: 1.03x slower                                                     |
| regex_v8       | 9.59 ms                                                  | 10.0 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.2 ms: 1.39x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.0 ms: 1.15x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 38.3 ms: 1.02x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.8 ms: 1.04x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.00 sec: 1.05x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.9 us: 1.10x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 114 us: 1.11x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 163 us: 1.17x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 5.13 ms: 1.21x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.55 ms: 1.19x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.58 ms: 1.33x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.26x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 24.6 ms: 1.13x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 12.0 ms: 1.14x slower                                                    |
| mako            | 4.77 ms                                                  | 5.77 ms: 1.21x slower                                                    |
| django_template | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.18x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 758 us: 2.65x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 205 ms: 2.35x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 216 ms: 2.30x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 9.10 ms: 2.28x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 204 ms: 2.18x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 220 ms: 2.09x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 90.8 ms: 1.90x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 459 us: 1.81x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 131 ms: 1.77x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 107 ms: 1.66x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.61x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.41x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.2 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 248 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| deepcopy                         | 161 us                                                   | 130 us: 1.24x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 824 ns: 1.17x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 15.6 us: 1.17x faster                                                    |
| float                            | 37.9 ms                                                  | 32.4 ms: 1.17x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.0 ms: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 118 ms: 1.12x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.86 us: 1.11x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.2 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.51 ms: 1.10x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.32 us: 1.10x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.02 sec: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.07 sec: 1.08x faster                                                   |
| pylint                           | 128 ms                                                   | 120 ms: 1.07x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 51.5 ms: 1.05x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 57.9 ms: 1.05x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 48.8 ns: 1.04x faster                                                    |
| go                               | 70.0 ms                                                  | 68.2 ms: 1.03x faster                                                    |
| raytrace                         | 145 ms                                                   | 142 ms: 1.02x faster                                                     |
| pycparser                        | 497 ms                                                   | 488 ms: 1.02x faster                                                     |
| sphinx                           | 434 ms                                                   | 426 ms: 1.02x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 42.8 ms: 1.02x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 38.3 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| pyflate                          | 216 ms                                                   | 214 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.74 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| regex_compile                    | 54.6 ms                                                  | 56.0 ms: 1.03x slower                                                    |
| regex_dna                        | 99.6 ms                                                  | 102 ms: 1.03x slower                                                     |
| json                             | 1.93 ms                                                  | 2.00 ms: 1.04x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.67 us: 1.04x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.8 ms: 1.04x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.92 us: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 336 us: 1.04x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 10.0 ms: 1.04x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 1.00 sec: 1.05x slower                                                   |
| mdp                              | 1.09 sec                                                 | 1.15 sec: 1.05x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 41.9 ms: 1.06x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 75.0 us: 1.06x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 24.5 ms: 1.07x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.6 ms: 1.07x slower                                                    |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                     |
| scimark_fft                      | 142 ms                                                   | 152 ms: 1.07x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.62 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.0 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 230 ms: 1.08x slower                                                     |
| sympy_str                        | 104 ms                                                   | 113 ms: 1.09x slower                                                     |
| chaos                            | 28.9 ms                                                  | 31.5 ms: 1.09x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.27 ms: 1.09x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 56.2 ms: 1.10x slower                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 51.3 ms: 1.10x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.9 us: 1.10x slower                                                    |
| 2to3                             | 114 ms                                                   | 126 ms: 1.10x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.36 ms: 1.10x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 35.6 ms: 1.11x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 114 us: 1.11x slower                                                     |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.80 ms: 1.12x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 24.6 ms: 1.13x slower                                                    |
| richards                         | 22.4 ms                                                  | 25.4 ms: 1.13x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 28.9 ms: 1.14x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 12.0 ms: 1.14x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 192 ms: 1.15x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 52.8 ms: 1.16x slower                                                    |
| nbody                            | 54.2 ms                                                  | 63.3 ms: 1.17x slower                                                    |
| fannkuch                         | 176 ms                                                   | 205 ms: 1.17x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 163 us: 1.17x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 388 ms: 1.18x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.55 ms: 1.19x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 798 ms: 1.20x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 5.13 ms: 1.21x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 57.7 ms: 1.21x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.77 ms: 1.21x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                    |
| many_optionals                   | 195 us                                                   | 250 us: 1.28x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.44 ms: 1.32x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.58 ms: 1.33x slower                                                    |
| coverage                         | 26.9 ms                                                  | 36.2 ms: 1.35x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 614 us: 1.47x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.5 ms: 2.54x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.04x faster                                                             |
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250314-3.14.0a5+-ca1bedc-NOGIL/bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.047x faster

# HPT report

- Reliability score: 53.78% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x