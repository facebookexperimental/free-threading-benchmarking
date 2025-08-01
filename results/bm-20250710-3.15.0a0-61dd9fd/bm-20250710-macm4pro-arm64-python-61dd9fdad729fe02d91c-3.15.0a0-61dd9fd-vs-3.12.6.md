# Results vs. 3.12.6

- fork: python
- ref: 61dd9fdad729fe02d91c
- machine: darwin-arm64
- commit hash: 61dd9fd
- commit date: 2025-07-10
- overall geometric mean: 1.111x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 407 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 244 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.84x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.99 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.18x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.1 ms: 1.08x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.3 ms: 1.25x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.2 ms: 1.15x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.4 ms: 1.13x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.7 ms: 1.01x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.74 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 45.2 ms: 1.14x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.1 ms: 1.07x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 97.0 us: 1.06x faster                                                   |
| tomli_loads          | 957 ms                                                   | 903 ms: 1.06x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 65.5 ms: 1.04x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.9 us: 1.01x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.43 ms: 1.04x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.68 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.22 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.89 ms: 1.06x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.6 ms: 1.01x faster                                                   |
| mako            | 4.77 ms                                                  | 4.89 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.70 ms: 2.14x faster                                                   |
| mdp                              | 1.09 sec                                                 | 512 ms: 2.13x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 244 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.84x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.46x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.46x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.99 ms: 1.36x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.29 us: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 40.3 ns: 1.26x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.4 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| float                            | 37.9 ms                                                  | 30.3 ms: 1.25x faster                                                   |
| go                               | 70.0 ms                                                  | 56.5 ms: 1.24x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 44.4 ms: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 119 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.9 ms: 1.22x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 950 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.18x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.8 ms: 1.15x faster                                                   |
| nbody                            | 54.2 ms                                                  | 47.2 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| typing_runtime_protocols         | 71.0 us                                                  | 62.0 us: 1.15x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.14x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.2 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| pylint                           | 128 ms                                                   | 113 ms: 1.13x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.4 ms: 1.13x faster                                                   |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.0 ms: 1.11x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.2 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.88 ms: 1.10x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.76 ms: 1.10x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.57 us: 1.09x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.36 us: 1.09x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.1 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.48 ms: 1.07x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 133 ms: 1.07x faster                                                    |
| sphinx                           | 434 ms                                                   | 407 ms: 1.07x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.1 ms: 1.07x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 97.0 us: 1.06x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 903 ms: 1.06x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.89 ms: 1.06x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.4 ms: 1.06x faster                                                   |
| thrift                           | 322 us                                                   | 304 us: 1.06x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.4 ms: 1.05x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.4 ms: 1.04x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 65.5 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.7 ms: 1.03x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.8 ms: 1.03x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.0 ms: 1.03x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.6 ms: 1.01x faster                                                   |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 98.7 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 660 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 326 ms: 1.01x faster                                                    |
| connected_components             | 201 ms                                                   | 201 ms: 1.00x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.0 ms: 1.01x slower                                                   |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| json_loads                       | 10.9 us                                                  | 10.9 us: 1.01x slower                                                   |
| fannkuch                         | 176 ms                                                   | 178 ms: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.74 ms: 1.02x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.89 ms: 1.02x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                  |
| bench_thread_pool                | 419 us                                                   | 434 us: 1.04x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.09 ms: 1.04x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.43 ms: 1.04x slower                                                   |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.68 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.22 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.3 ms: 1.11x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 956 us: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.0 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 245 us: 1.25x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                            |

Benchmark hidden because not significant (4): json, sqlite_synth, sympy_expand, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.111x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x