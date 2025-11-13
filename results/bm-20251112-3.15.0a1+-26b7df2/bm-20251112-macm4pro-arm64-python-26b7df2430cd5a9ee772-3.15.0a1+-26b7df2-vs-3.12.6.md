# Results vs. 3.12.6

- fork: python
- ref: 26b7df2430cd5a9ee772
- machine: darwin-arm64
- commit hash: 26b7df2
- commit date: 2025-11-12
- overall geometric mean: 1.111x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.00x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 403 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 232 ms: 2.14x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.10x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 233 ms: 1.97x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 229 ms: 1.95x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.71x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.64x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 143 ms: 1.56x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 43.1 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.0 ms: 2.58x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.30x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                    |
| nbody          | 54.2 ms                                                  | 47.7 ms: 1.14x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.14x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 48.8 ms: 1.12x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.8 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.90 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.4 ms: 1.28x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.3 ms: 1.10x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.94 ms: 1.08x faster                                                    |
| tomli_loads          | 957 ms                                                   | 894 ms: 1.07x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 65.4 ms: 1.04x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 99.4 us: 1.04x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.32 ms: 1.11x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.92 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.99 ms: 1.05x faster                                                    |
| mako            | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.14x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 232 ms: 2.14x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.10x faster                                                     |
| mdp                              | 1.09 sec                                                 | 541 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 233 ms: 1.97x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 229 ms: 1.95x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.71x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.64x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 143 ms: 1.56x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.8 us: 1.55x faster                                                    |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                     |
| float                            | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.47 us: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.13 us: 1.29x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.4 ms: 1.28x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.0 ms: 1.26x faster                                                    |
| go                               | 70.0 ms                                                  | 55.5 ms: 1.26x faster                                                    |
| raytrace                         | 145 ms                                                   | 117 ms: 1.24x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 41.2 ns: 1.24x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.8 ms: 1.22x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.2 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.48 ms: 1.16x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.79 ms: 1.16x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 18.0 ms: 1.16x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                     |
| pylint                           | 128 ms                                                   | 112 ms: 1.14x faster                                                     |
| nbody                            | 54.2 ms                                                  | 47.7 ms: 1.14x faster                                                    |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.13x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.6 ms: 1.13x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.6 ms: 1.13x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.30 us: 1.12x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.8 ms: 1.12x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.53 us: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.02 sec: 1.11x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.3 ms: 1.10x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.5 ms: 1.09x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.9 ms: 1.09x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 65.4 us: 1.09x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.94 ms: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 403 ms: 1.08x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 894 ms: 1.07x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 23.9 ms: 1.06x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.86 ms: 1.06x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.2 ms: 1.06x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.1 ms: 1.06x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.60 ms: 1.06x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 48.8 ms: 1.05x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.99 ms: 1.05x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 65.4 ms: 1.04x faster                                                    |
| pycparser                        | 497 ms                                                   | 480 ms: 1.04x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 99.4 us: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 96.8 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| thrift                           | 322 us                                                   | 319 us: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                     |
| sympy_str                        | 104 ms                                                   | 104 ms: 1.01x faster                                                     |
| 2to3                             | 114 ms                                                   | 115 ms: 1.00x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 670 ms: 1.01x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                    |
| sqlite_synth                     | 967 ns                                                   | 980 ns: 1.01x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 333 ms: 1.02x slower                                                     |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.90 ms: 1.03x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 432 us: 1.03x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.09 ms: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                     |
| fannkuch                         | 176 ms                                                   | 184 ms: 1.05x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 175 ms: 1.05x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.7 ms: 1.06x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.89 ms: 1.11x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.32 ms: 1.11x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.1 ms: 1.11x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.92 ms: 1.11x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.12x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 933 us: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.14x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.4 ms: 1.24x slower                                                    |
| many_optionals                   | 195 us                                                   | 364 us: 1.87x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.0 ms: 2.58x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (2): sympy_sum, html5lib
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251112-3.15.0a1+-26b7df2/bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.111x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.22x