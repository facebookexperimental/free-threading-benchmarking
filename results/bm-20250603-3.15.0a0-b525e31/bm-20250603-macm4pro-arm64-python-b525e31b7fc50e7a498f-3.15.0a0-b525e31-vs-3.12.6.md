# Results vs. 3.12.6

- fork: python
- ref: b525e31b7fc50e7a498f
- machine: darwin-arm64
- commit hash: b525e31
- commit date: 2025-06-03
- overall geometric mean: 1.120x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 405 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 240 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                    |
| async_generators                 | 206 ms                                                   | 170 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.7 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.3 ms: 2.69x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.4 ms: 1.29x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.3 ms: 1.15x faster                                                   |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.0 ms: 1.16x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.1 ms: 1.03x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.91 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.6 ms: 1.16x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 62.4 ms: 1.09x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                   |
| tomli_loads          | 957 ms                                                   | 893 ms: 1.07x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 96.6 us: 1.07x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 4.39 ms: 1.03x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.58 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.15 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.78 ms: 1.07x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                   |
| mako            | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                   |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.11x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.47 ms: 2.19x faster                                                   |
| mdp                              | 1.09 sec                                                 | 507 ms: 2.15x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 240 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.1 us: 1.51x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| deepcopy                         | 161 us                                                   | 107 us: 1.51x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.40 us: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.30x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.12 us: 1.30x faster                                                   |
| float                            | 37.9 ms                                                  | 29.4 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.2 ms: 1.28x faster                                                   |
| go                               | 70.0 ms                                                  | 55.5 ms: 1.26x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 170 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.3 ms: 1.21x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 17.6 ms: 1.21x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.9 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 948 ms: 1.18x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.49 ms: 1.16x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 47.0 ms: 1.16x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.6 ms: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| nbody                            | 54.2 ms                                                  | 47.3 ms: 1.15x faster                                                   |
| pylint                           | 128 ms                                                   | 113 ms: 1.14x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.2 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.5 us: 1.13x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.70 ms: 1.13x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.84 ms: 1.13x faster                                                   |
| pyflate                          | 216 ms                                                   | 193 ms: 1.12x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.7 ms: 1.12x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.1 ms: 1.11x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 46.7 ms: 1.10x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.7 ms: 1.09x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 62.4 ms: 1.09x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.37 ms: 1.09x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                    |
| thrift                           | 322 us                                                   | 300 us: 1.07x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 893 ms: 1.07x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.78 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 405 ms: 1.07x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 96.6 us: 1.07x faster                                                   |
| sympy_str                        | 104 ms                                                   | 98.0 ms: 1.06x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.0 ms: 1.05x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.3 ms: 1.05x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.4 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.3 ms: 1.04x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.49 us: 1.03x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.73 us: 1.03x faster                                                   |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 97.1 ms: 1.03x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 953 ns: 1.01x faster                                                    |
| pycparser                        | 497 ms                                                   | 492 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.01x faster                                                    |
| meteor_contest                   | 47.7 ms                                                  | 47.9 ms: 1.00x slower                                                   |
| connected_components             | 201 ms                                                   | 202 ms: 1.00x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                  |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.06 ms: 1.02x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.39 ms: 1.03x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.03x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.91 ms: 1.03x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 710 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.58 ms: 1.07x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 353 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.15 ms: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.8 ms: 1.10x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 921 us: 1.11x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.11x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 241 us: 1.23x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.3 ms: 2.69x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 195 ns: 3.84x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, shortest_path
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250603-3.15.0a0-b525e31/bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.120x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.14x