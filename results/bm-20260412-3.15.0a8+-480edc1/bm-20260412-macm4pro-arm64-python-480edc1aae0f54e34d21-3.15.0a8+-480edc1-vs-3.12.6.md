# Results vs. 3.12.6

- fork: python
- ref: 480edc1aae0f54e34d21
- machine: darwin-arm64
- commit hash: 480edc1
- commit date: 2026-04-12
- overall geometric mean: 1.154x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.03x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.6 ms: 1.07x faster                                                    |
| sphinx         | 434 ms                                                   | 400 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 224 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.11x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 236 ms: 1.95x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.70x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.64x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 250 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.0 ms: 1.11x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.3 ms: 2.59x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.32x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| nbody          | 54.2 ms                                                  | 45.1 ms: 1.20x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.18x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.77 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.2 ms: 1.31x faster                                                    |
| tomli_loads          | 957 ms                                                   | 827 ms: 1.16x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.76 ms: 1.13x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                     |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.85 ms: 1.10x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.36 ms: 1.12x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.81 ms: 1.07x faster                                                    |
| mako            | 4.77 ms                                                  | 4.72 ms: 1.01x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.5 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 14.9 ms: 1.09x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.00x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.99 ms: 5.20x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 224 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.11x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.03x faster                                                     |
| mdp                              | 1.09 sec                                                 | 542 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 236 ms: 1.95x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.70x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.64x faster                                                     |
| deepcopy                         | 161 us                                                   | 98.5 us: 1.64x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.6 us: 1.57x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.06 us: 1.39x faster                                                    |
| float                            | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 250 ms: 1.35x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.08 us: 1.35x faster                                                    |
| go                               | 70.0 ms                                                  | 52.6 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.2 ms: 1.31x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 42.6 ms: 1.28x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 48.9 ms: 1.25x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.1 ns: 1.24x faster                                                    |
| k_core                           | 1.12 sec                                                 | 911 ms: 1.23x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 117 ms: 1.21x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 35.8 ms: 1.21x faster                                                    |
| nbody                            | 54.2 ms                                                  | 45.1 ms: 1.20x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.3 ms: 1.19x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.19x faster                                                    |
| pyflate                          | 216 ms                                                   | 183 ms: 1.18x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.7 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.21 us: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 827 ms: 1.16x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 44.3 ms: 1.16x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.43 us: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.2 ms: 1.14x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.76 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.0 ms: 1.11x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 64.5 us: 1.10x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.89 ms: 1.10x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.76 ms: 1.10x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.3 ms: 1.09x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.7 ms: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 400 ms: 1.08x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.81 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 467 ms: 1.07x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.6 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.60 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.06x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 631 ms: 1.05x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 313 ms: 1.05x faster                                                     |
| fannkuch                         | 176 ms                                                   | 169 ms: 1.04x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                     |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 56.4 ms: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 948 ns: 1.02x faster                                                     |
| thrift                           | 322 us                                                   | 316 us: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.72 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.5 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.01x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 39.2 ms: 1.01x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.77 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.02x slower                                                     |
| 2to3                             | 114 ms                                                   | 117 ms: 1.03x slower                                                     |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 173 ms: 1.03x slower                                                     |
| connected_components             | 201 ms                                                   | 209 ms: 1.04x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.6 ms: 1.06x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.83 ms: 1.08x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.9 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.85 ms: 1.10x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.36 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 961 us: 1.16x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 46.3 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.0 ms: 1.19x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.45 ms: 1.22x slower                                                    |
| many_optionals                   | 195 us                                                   | 253 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.3 ms: 2.59x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                             |

Benchmark hidden because not significant (1): json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260412-3.15.0a8+-480edc1/bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.154x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.24x