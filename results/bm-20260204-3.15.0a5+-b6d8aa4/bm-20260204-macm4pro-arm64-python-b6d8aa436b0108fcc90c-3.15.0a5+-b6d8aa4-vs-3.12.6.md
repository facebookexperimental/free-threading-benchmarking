# Results vs. 3.12.6

- fork: python
- ref: b6d8aa436b0108fcc90c
- machine: darwin-arm64
- commit hash: b6d8aa4
- commit date: 2026-02-04
- overall geometric mean: 1.196x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 107 ms: 1.07x faster                                                     |
| docutils       | 1.02 sec                                                 | 975 ms: 1.05x faster                                                     |
| html5lib       | 23.0 ms                                                  | 20.7 ms: 1.11x faster                                                    |
| sphinx         | 434 ms                                                   | 378 ms: 1.15x faster                                                     |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 213 ms: 2.33x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 222 ms: 2.16x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 220 ms: 2.09x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 214 ms: 2.08x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 95.4 ms: 1.81x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 98.9 ms: 1.80x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 133 ms: 1.73x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 243 ms: 1.39x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.27x faster                                                     |
| async_generators                 | 206 ms                                                   | 169 ms: 1.22x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 38.8 ms: 1.17x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 211 ms: 1.09x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 181 ms: 1.05x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 116 ms: 1.03x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.2 ms: 2.40x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| nbody          | 54.2 ms                                                  | 43.3 ms: 1.25x faster                                                    |
| pidigits       | 161 ms                                                   | 156 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.21x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.8 ms: 1.25x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 91.2 ms: 1.09x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.53 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.6 ms: 1.34x faster                                                    |
| tomli_loads          | 957 ms                                                   | 814 ms: 1.18x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 33.8 ms: 1.15x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.71 ms: 1.15x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.0 ms: 1.12x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 95.3 us: 1.08x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.3 us: 1.05x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 137 us: 1.02x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.25 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.45 ms: 1.11x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.4 ms: 1.07x faster                                                    |
| mako            | 4.77 ms                                                  | 4.57 ms: 1.04x faster                                                    |
| django_template | 13.6 ms                                                  | 14.3 ms: 1.05x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.04x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.81 ms: 5.45x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 213 ms: 2.33x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 222 ms: 2.16x faster                                                     |
| mdp                              | 1.09 sec                                                 | 521 ms: 2.10x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 220 ms: 2.09x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 214 ms: 2.08x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 95.4 ms: 1.81x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 98.9 ms: 1.80x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 133 ms: 1.73x faster                                                     |
| deepcopy                         | 161 us                                                   | 94.7 us: 1.71x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.1 us: 1.66x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 6.98 us: 1.41x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.05 us: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 243 ms: 1.39x faster                                                     |
| go                               | 70.0 ms                                                  | 50.9 ms: 1.38x faster                                                    |
| float                            | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.6 ms: 1.34x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.27x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.4 ns: 1.26x faster                                                    |
| k_core                           | 1.12 sec                                                 | 892 ms: 1.25x faster                                                     |
| nbody                            | 54.2 ms                                                  | 43.3 ms: 1.25x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 43.8 ms: 1.25x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.39 ms: 1.24x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.3 ms: 1.24x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.8 ms: 1.23x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.4 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 169 ms: 1.22x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.13 us: 1.21x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.33 us: 1.20x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.8 ms: 1.19x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 43.0 ms: 1.19x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 814 ms: 1.18x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.17x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 38.8 ms: 1.17x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 21.7 ms: 1.17x faster                                                    |
| pyflate                          | 216 ms                                                   | 185 ms: 1.17x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.7 ms: 1.16x faster                                                    |
| richards                         | 22.4 ms                                                  | 19.3 ms: 1.16x faster                                                    |
| pylint                           | 128 ms                                                   | 110 ms: 1.16x faster                                                     |
| chaos                            | 28.9 ms                                                  | 25.1 ms: 1.15x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 33.8 ms: 1.15x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 61.7 us: 1.15x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.71 ms: 1.15x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.9 ms: 1.15x faster                                                    |
| sphinx                           | 434 ms                                                   | 378 ms: 1.15x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.67 ms: 1.14x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.0 ms: 1.12x faster                                                    |
| pycparser                        | 497 ms                                                   | 448 ms: 1.11x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 20.7 ms: 1.11x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.45 ms: 1.11x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.87 ms: 1.11x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 297 ms: 1.11x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.26 ms: 1.10x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 603 ms: 1.10x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 91.2 ms: 1.09x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 211 ms: 1.09x faster                                                     |
| thrift                           | 322 us                                                   | 297 us: 1.08x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 95.3 us: 1.08x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 53.5 ms: 1.08x faster                                                    |
| sympy_str                        | 104 ms                                                   | 97.5 ms: 1.07x faster                                                    |
| 2to3                             | 114 ms                                                   | 107 ms: 1.07x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 20.4 ms: 1.07x faster                                                    |
| fannkuch                         | 176 ms                                                   | 165 ms: 1.06x faster                                                     |
| json                             | 1.93 ms                                                  | 1.82 ms: 1.06x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 181 ms: 1.05x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.3 us: 1.05x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 920 ns: 1.05x faster                                                     |
| docutils                         | 1.02 sec                                                 | 975 ms: 1.05x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.57 ms: 1.04x faster                                                    |
| pidigits                         | 161 ms                                                   | 156 ms: 1.04x faster                                                     |
| gc_traversal                     | 2.01 ms                                                  | 1.97 ms: 1.02x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 137 us: 1.02x faster                                                     |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.01x faster                                                     |
| meteor_contest                   | 47.7 ms                                                  | 47.4 ms: 1.01x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.53 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 116 ms: 1.03x slower                                                     |
| connected_components             | 201 ms                                                   | 208 ms: 1.04x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.3 ms: 1.05x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.75 ms: 1.06x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 878 us: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 43.3 ms: 1.09x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.25 ms: 1.09x slower                                                    |
| coverage                         | 26.9 ms                                                  | 30.6 ms: 1.14x slower                                                    |
| many_optionals                   | 195 us                                                   | 235 us: 1.20x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.2 ms: 2.40x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.19x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260204-3.15.0a5+-b6d8aa4/bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.196x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.23x