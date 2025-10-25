# Results vs. 3.12.6

- fork: python
- ref: d78d7a50b06c4ea10d13
- machine: darwin-arm64
- commit hash: d78d7a5
- commit date: 2025-10-24
- overall geometric mean: 1.130x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.00x slower                                                   |
| html5lib       | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 395 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 225 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 222 ms: 2.16x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 228 ms: 2.02x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 225 ms: 1.98x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.9 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 139 ms: 1.66x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 141 ms: 1.58x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.8 ms: 1.09x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 125 ms: 1.11x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.4 ms: 2.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.31x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.1 ms: 1.40x faster                                                    |
| nbody          | 54.2 ms                                                  | 48.8 ms: 1.11x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.15x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.3 ms: 1.18x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.18x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.7 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.67 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.6 ms: 1.33x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.0 ms: 1.14x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.9 ms: 1.13x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.89 ms: 1.10x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                    |
| tomli_loads          | 957 ms                                                   | 886 ms: 1.08x faster                                                     |
| unpickle_pure_python | 103 us                                                   | 98.1 us: 1.05x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.21 ms: 1.09x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.75 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.70 ms: 1.08x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.2 ms: 1.03x faster                                                    |
| mako            | 4.77 ms                                                  | 4.73 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.00x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 225 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 222 ms: 2.16x faster                                                     |
| mdp                              | 1.09 sec                                                 | 533 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 228 ms: 2.02x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 225 ms: 1.98x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.9 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 139 ms: 1.66x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.59x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 141 ms: 1.58x faster                                                     |
| deepcopy                         | 161 us                                                   | 103 us: 1.56x faster                                                     |
| float                            | 37.9 ms                                                  | 27.1 ms: 1.40x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.30 us: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.6 ms: 1.33x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.10 us: 1.33x faster                                                    |
| go                               | 70.0 ms                                                  | 53.1 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 39.9 ns: 1.28x faster                                                    |
| raytrace                         | 145 ms                                                   | 116 ms: 1.25x faster                                                     |
| k_core                           | 1.12 sec                                                 | 905 ms: 1.24x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 44.5 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.9 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.4 ms: 1.19x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.3 ms: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.18x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.8 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| chaos                            | 28.9 ms                                                  | 25.1 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.0 ms: 1.14x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.47 us: 1.14x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.9 ms: 1.13x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.27 us: 1.13x faster                                                    |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.13x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 63.3 us: 1.12x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.7 ms: 1.12x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.9 ms: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.72 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                     |
| nbody                            | 54.2 ms                                                  | 48.8 ms: 1.11x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.88 ms: 1.11x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.3 ms: 1.10x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.0 ms: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 395 ms: 1.10x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.89 ms: 1.10x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.8 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.39 ms: 1.09x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.70 ms: 1.08x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 886 ms: 1.08x faster                                                     |
| pycparser                        | 497 ms                                                   | 466 ms: 1.07x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 48.2 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.7 ms: 1.06x faster                                                    |
| thrift                           | 322 us                                                   | 307 us: 1.05x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 98.1 us: 1.05x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.1 ms: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.2 ms: 1.04x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 638 ms: 1.04x faster                                                     |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 315 ms: 1.04x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.2 ms: 1.03x faster                                                    |
| bench_thread_pool                | 419 us                                                   | 411 us: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.73 ms: 1.01x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 960 ns: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.00x slower                                                   |
| shortest_path                    | 219 ms                                                   | 220 ms: 1.01x slower                                                     |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.01x slower                                                     |
| connected_components             | 201 ms                                                   | 202 ms: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.67 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 48.6 ms: 1.02x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 41.3 ms: 1.04x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.14 ms: 1.07x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.21 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.75 ms: 1.09x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.88 ms: 1.10x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 919 us: 1.11x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 125 ms: 1.11x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.2 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 362 us: 1.85x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.4 ms: 2.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                             |

Benchmark hidden because not significant (2): json, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251024-3.15.0a1+-d78d7a5/bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.130x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.20x