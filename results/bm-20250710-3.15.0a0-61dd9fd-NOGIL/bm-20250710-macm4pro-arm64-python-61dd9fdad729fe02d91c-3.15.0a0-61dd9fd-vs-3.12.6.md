# Results vs. 3.12.6

- fork: python
- ref: 61dd9fdad729fe02d91c
- machine: darwin-arm64
- commit hash: 61dd9fd
- commit date: 2025-07-10
- overall geometric mean: 1.102x faster
- HPT reliability: 98.37%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                  |
| sphinx         | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.29x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.7 ms: 1.99x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.4 ms: 1.08x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.34x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| nbody          | 54.2 ms                                                  | 55.8 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.2 ms: 1.05x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.24 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.9 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.1 ms: 1.39x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 56.9 ms: 1.19x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                   |
| tomli_loads          | 957 ms                                                   | 977 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.6 us: 1.06x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 151 us: 1.08x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.63 ms: 1.09x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.58 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.95 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.4 ms: 1.07x slower                                                   |
| mako            | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                   |
| django_template | 13.6 ms                                                  | 16.2 ms: 1.19x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 784 us: 2.56x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.29x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.84 ms: 2.11x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 86.7 ms: 1.99x faster                                                   |
| mdp                              | 1.09 sec                                                 | 572 ms: 1.91x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.72x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 492 us: 1.69x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.1 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.6 us: 1.35x faster                                                   |
| deepcopy                         | 161 us                                                   | 120 us: 1.34x faster                                                    |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.34x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.99 us: 1.23x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 56.9 ms: 1.19x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 822 ns: 1.18x faster                                                    |
| go                               | 70.0 ms                                                  | 59.9 ms: 1.17x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.1 ns: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 993 ms: 1.13x faster                                                    |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                    |
| pyflate                          | 216 ms                                                   | 194 ms: 1.11x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.2 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 131 ms: 1.10x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                   |
| pycparser                        | 497 ms                                                   | 467 ms: 1.06x faster                                                    |
| sphinx                           | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.5 ms: 1.06x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 52.2 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.24 ms: 1.04x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 42.1 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.9 ms: 1.02x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                  |
| scimark_fft                      | 142 ms                                                   | 140 ms: 1.01x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 3.01 ms: 1.01x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.00 ms: 1.00x faster                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.59 us: 1.01x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.2 ms: 1.01x slower                                                   |
| fannkuch                         | 176 ms                                                   | 178 ms: 1.01x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 977 ms: 1.02x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.88 us: 1.03x slower                                                   |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| nbody                            | 54.2 ms                                                  | 55.8 ms: 1.03x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.2 ms: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 332 us: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.4 us: 1.03x slower                                                   |
| json                             | 1.93 ms                                                  | 2.01 ms: 1.04x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 343 ms: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.4 ms: 1.04x slower                                                   |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 697 ms: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.5 ms: 1.05x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.8 ms: 1.05x slower                                                   |
| shortest_path                    | 219 ms                                                   | 232 ms: 1.06x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.6 us: 1.06x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 54.8 ms: 1.07x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.4 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.24 ms: 1.08x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 151 us: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.4 ms: 1.08x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.63 ms: 1.09x slower                                                   |
| connected_components             | 201 ms                                                   | 220 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.8 ms: 1.10x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.8 ms: 1.13x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 54.3 ms: 1.14x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.2 ms: 1.19x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.58 ms: 1.19x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.95 ms: 1.22x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.21 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 250 us: 1.28x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 578 us: 1.38x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.3 ms: 1.50x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (1): html5lib
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.102x faster

# HPT report

- Reliability score: 98.37% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x