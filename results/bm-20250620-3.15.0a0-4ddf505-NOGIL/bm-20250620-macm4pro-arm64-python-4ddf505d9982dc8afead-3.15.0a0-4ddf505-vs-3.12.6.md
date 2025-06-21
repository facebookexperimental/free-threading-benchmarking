# Results vs. 3.12.6

- fork: python
- ref: 4ddf505d9982dc8afead
- machine: darwin-arm64
- commit hash: 4ddf505
- commit date: 2025-06-20
- overall geometric mean: 1.096x faster
- HPT reliability: 97.56%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| docutils       | 1.02 sec                                                 | 999 ms: 1.02x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 419 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.5 ms: 1.97x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.16x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.2 ms: 1.08x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.2 ms: 1.35x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| nbody          | 54.2 ms                                                  | 56.1 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.23 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.9 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.7 ms: 1.18x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.2 ms: 1.02x slower                                                   |
| tomli_loads          | 957 ms                                                   | 988 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.59 ms: 1.08x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 154 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.53 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.94 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.20x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.08x slower                                                   |
| mako            | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                   |
| django_template | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 781 us: 2.57x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.69 ms: 2.14x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 87.5 ms: 1.97x faster                                                   |
| mdp                              | 1.09 sec                                                 | 560 ms: 1.95x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 488 us: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| deepcopy                         | 161 us                                                   | 120 us: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| float                            | 37.9 ms                                                  | 28.2 ms: 1.35x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.7 us: 1.33x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.82 us: 1.26x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.7 ms: 1.18x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 823 ns: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.9 ms: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                  |
| async_generators                 | 206 ms                                                   | 179 ms: 1.16x faster                                                    |
| go                               | 70.0 ms                                                  | 61.1 ms: 1.15x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 982 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 54.7 ms: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 131 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 199 ms: 1.09x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.1 ms: 1.09x faster                                                   |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.7 ms: 1.07x faster                                                   |
| pycparser                        | 497 ms                                                   | 472 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.66 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.23 ms: 1.04x faster                                                   |
| sphinx                           | 434 ms                                                   | 419 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.9 ms: 1.03x faster                                                   |
| docutils                         | 1.02 sec                                                 | 999 ms: 1.02x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.99 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 140 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.95 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 71.5 us: 1.01x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.3 ms: 1.01x slower                                                   |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.2 ms: 1.02x slower                                                   |
| thrift                           | 322 us                                                   | 328 us: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.1 ms: 1.03x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 988 ms: 1.03x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.1 ms: 1.03x slower                                                   |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.6 ms: 1.05x slower                                                   |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 232 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.21 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 41.7 ms: 1.07x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.59 ms: 1.08x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.2 ms: 1.08x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.08x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.80 us: 1.09x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.5 ms: 1.09x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.9 ms: 1.10x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 154 us: 1.10x slower                                                    |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.12 us: 1.11x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 53.3 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.5 ms: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.12x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 376 ms: 1.15x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 767 ms: 1.15x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.53 ms: 1.19x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.94 ms: 1.22x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.26 ms: 1.25x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 64.6 ms: 1.26x slower                                                   |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 595 us: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.6 ms: 1.47x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 218 ns: 4.28x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.096x faster

# HPT report

- Reliability score: 97.56% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x