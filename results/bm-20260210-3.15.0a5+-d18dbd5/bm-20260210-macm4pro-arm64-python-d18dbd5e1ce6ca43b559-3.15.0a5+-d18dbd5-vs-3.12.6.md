# Results vs. 3.12.6

- fork: python
- ref: d18dbd5e1ce6ca43b559
- machine: darwin-arm64
- commit hash: d18dbd5
- commit date: 2026-02-10
- overall geometric mean: 1.172x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.1 ms: 1.09x faster                                                    |
| sphinx         | 434 ms                                                   | 389 ms: 1.12x faster                                                     |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.12x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 225 ms: 2.04x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.01x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 96.5 ms: 1.78x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 138 ms: 1.62x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.98 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 250 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.26x faster                                                     |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.6 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.10x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.9 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.5 ms: 1.38x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.2 ms: 1.23x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                    | 1.19x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 44.9 ms: 1.22x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.5 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| tomli_loads          | 957 ms                                                   | 834 ms: 1.15x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 59.5 ms: 1.14x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.82 ms: 1.11x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.4 ms: 1.10x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 95.9 us: 1.07x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.02x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 138 us: 1.01x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.30 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.53 ms: 1.10x faster                                                    |
| mako            | 4.77 ms                                                  | 4.58 ms: 1.04x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| django_template | 13.6 ms                                                  | 14.5 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.03x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.96 ms: 5.24x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.12x faster                                                     |
| mdp                              | 1.09 sec                                                 | 531 ms: 2.06x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 225 ms: 2.04x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.01x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 96.5 ms: 1.78x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                     |
| deepcopy                         | 161 us                                                   | 97.0 us: 1.66x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.2 us: 1.63x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 138 ms: 1.62x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 6.99 us: 1.41x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.06 us: 1.38x faster                                                    |
| float                            | 37.9 ms                                                  | 27.5 ms: 1.38x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.98 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 250 ms: 1.35x faster                                                     |
| go                               | 70.0 ms                                                  | 52.6 ms: 1.33x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                                     |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.26x faster                                                     |
| k_core                           | 1.12 sec                                                 | 896 ms: 1.25x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.7 ms: 1.24x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.2 ms: 1.24x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.2 ns: 1.24x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.2 ms: 1.23x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 44.9 ms: 1.22x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 118 ms: 1.21x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.3 ms: 1.20x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                    |
| pyflate                          | 216 ms                                                   | 184 ms: 1.17x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.19 us: 1.17x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.77 ms: 1.17x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.6 ms: 1.17x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.41 us: 1.16x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 834 ms: 1.15x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 59.5 ms: 1.14x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.3 ms: 1.14x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 45.0 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                   |
| pylint                           | 128 ms                                                   | 113 ms: 1.13x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 38.4 ms: 1.13x faster                                                    |
| richards                         | 22.4 ms                                                  | 19.9 ms: 1.13x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.8 ms: 1.12x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.6 ms: 1.12x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.6 us: 1.12x faster                                                    |
| sphinx                           | 434 ms                                                   | 389 ms: 1.12x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.82 ms: 1.11x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.74 ms: 1.11x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.53 ms: 1.10x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.4 ms: 1.10x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.1 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.36 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 458 ms: 1.09x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 95.9 us: 1.07x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 624 ms: 1.07x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 308 ms: 1.06x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 54.5 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.5 ms: 1.05x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.1 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| thrift                           | 322 us                                                   | 308 us: 1.05x faster                                                     |
| fannkuch                         | 176 ms                                                   | 168 ms: 1.05x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.58 ms: 1.04x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 933 ns: 1.04x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.7 ms: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 138 us: 1.01x faster                                                     |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.04 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 48.9 ms: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 206 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.79 ms: 1.07x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.5 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 912 us: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.10x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.30 ms: 1.10x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.0 ms: 1.13x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.2 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 251 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.9 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.17x faster                                                             |

Benchmark hidden because not significant (2): sympy_expand, regex_v8
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260210-3.15.0a5+-d18dbd5/bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.172x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.22x