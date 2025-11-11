# Results vs. 3.12.6

- fork: python
- ref: 86513f6c2ebdd1fb692c
- machine: darwin-arm64
- commit hash: 86513f6
- commit date: 2025-11-10
- overall geometric mean: 1.113x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 403 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 229 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 228 ms: 2.10x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 230 ms: 2.00x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 227 ms: 1.96x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 142 ms: 1.57x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.96 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 42.9 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.7 ms: 2.57x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.30x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| nbody          | 54.2 ms                                                  | 49.5 ms: 1.09x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 48.7 ms: 1.12x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.1 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.1 ms: 1.28x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.2 ms: 1.10x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 62.1 ms: 1.09x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.90 ms: 1.09x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.1 ms: 1.07x faster                                                    |
| tomli_loads          | 957 ms                                                   | 901 ms: 1.06x faster                                                     |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                     |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.01x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.27 ms: 1.10x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.86 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 22.1 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 229 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 228 ms: 2.10x faster                                                     |
| mdp                              | 1.09 sec                                                 | 539 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 230 ms: 2.00x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 227 ms: 1.96x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 142 ms: 1.57x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.1 us: 1.51x faster                                                    |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.96 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 7.40 us: 1.33x faster                                                    |
| float                            | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.1 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                    |
| go                               | 70.0 ms                                                  | 55.5 ms: 1.26x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.7 ms: 1.24x faster                                                    |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 41.3 ns: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.8 ms: 1.23x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.3 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.9 ms: 1.16x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.80 ms: 1.15x faster                                                    |
| pylint                           | 128 ms                                                   | 112 ms: 1.15x faster                                                     |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.7 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.01 sec: 1.12x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.31 us: 1.11x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.0 ms: 1.11x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.53 us: 1.11x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.2 ms: 1.10x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.3 ms: 1.10x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.6 ms: 1.10x faster                                                    |
| nbody                            | 54.2 ms                                                  | 49.5 ms: 1.09x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 62.1 ms: 1.09x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.5 ms: 1.09x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.90 ms: 1.09x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 65.2 us: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 403 ms: 1.07x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.83 ms: 1.07x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.1 ms: 1.07x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.9 ms: 1.06x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 901 ms: 1.06x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.56 ms: 1.06x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.2 ms: 1.06x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.0 ms: 1.06x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 48.8 ms: 1.05x faster                                                    |
| pycparser                        | 497 ms                                                   | 476 ms: 1.05x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.2 ms: 1.05x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.1 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                     |
| thrift                           | 322 us                                                   | 316 us: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 57.2 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 331 ms: 1.01x slower                                                     |
| sqlite_synth                     | 967 ns                                                   | 979 ns: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.1 ms: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.6 ms: 1.04x slower                                                    |
| fannkuch                         | 176 ms                                                   | 183 ms: 1.04x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 176 ms: 1.05x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 42.5 ms: 1.07x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.27 ms: 1.10x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.87 ms: 1.10x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.86 ms: 1.11x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 927 us: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| coverage                         | 26.9 ms                                                  | 33.7 ms: 1.25x slower                                                    |
| many_optionals                   | 195 us                                                   | 361 us: 1.85x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.7 ms: 2.57x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (5): bench_thread_pool, sympy_str, 2to3, pprint_pformat, mako
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251110-3.15.0a1+-86513f6/bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.113x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.21x