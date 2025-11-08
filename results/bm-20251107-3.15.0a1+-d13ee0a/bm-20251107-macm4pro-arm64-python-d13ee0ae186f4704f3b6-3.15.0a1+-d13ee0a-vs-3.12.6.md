# Results vs. 3.12.6

- fork: python
- ref: d13ee0ae186f4704f3b6
- machine: darwin-arm64
- commit hash: d13ee0a
- commit date: 2025-11-07
- overall geometric mean: 1.134x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 393 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 224 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 219 ms: 2.19x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 217 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 227 ms: 2.03x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.4 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.9 ms: 1.76x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.89 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 248 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.2 ms: 1.10x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.04x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 124 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 236 ms: 1.11x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.6 ms: 2.51x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.7 ms: 1.37x faster                                                    |
| nbody          | 54.2 ms                                                  | 48.6 ms: 1.12x faster                                                    |
| pidigits       | 161 ms                                                   | 158 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.16x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 47.9 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.8 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.65 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.0 ms: 1.11x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.87 ms: 1.10x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.8 ms: 1.10x faster                                                    |
| tomli_loads          | 957 ms                                                   | 890 ms: 1.08x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.3 us: 1.06x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.03x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.21 ms: 1.09x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.76 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.87 ms: 1.06x faster                                                    |
| mako            | 4.77 ms                                                  | 4.70 ms: 1.02x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.5 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 224 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 219 ms: 2.19x faster                                                     |
| mdp                              | 1.09 sec                                                 | 523 ms: 2.09x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 217 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 227 ms: 2.03x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.4 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.9 ms: 1.76x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.59x faster                                                    |
| deepcopy                         | 161 us                                                   | 106 us: 1.52x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.89 ms: 1.37x faster                                                    |
| float                            | 37.9 ms                                                  | 27.7 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 248 ms: 1.37x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 7.27 us: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.11 us: 1.32x faster                                                    |
| go                               | 70.0 ms                                                  | 54.4 ms: 1.29x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 39.7 ns: 1.28x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 48.6 ms: 1.26x faster                                                    |
| raytrace                         | 145 ms                                                   | 116 ms: 1.25x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.5 ms: 1.25x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.8 ms: 1.23x faster                                                    |
| k_core                           | 1.12 sec                                                 | 906 ms: 1.23x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.5 ms: 1.18x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.76 ms: 1.18x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 122 ms: 1.16x faster                                                     |
| pyflate                          | 216 ms                                                   | 187 ms: 1.15x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 47.9 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.26 us: 1.14x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.48 us: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                    |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.8 ms: 1.12x faster                                                    |
| nbody                            | 54.2 ms                                                  | 48.6 ms: 1.12x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.0 ms: 1.11x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.0 ms: 1.11x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.1 ms: 1.11x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.2 ms: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 393 ms: 1.10x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.87 ms: 1.10x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.5 us: 1.10x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.8 ms: 1.10x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 47.1 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.39 ms: 1.09x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.80 ms: 1.08x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.5 ms: 1.08x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.7 ms: 1.08x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 890 ms: 1.08x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 36.1 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 465 ms: 1.07x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 9.87 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.8 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 97.3 us: 1.06x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.04x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.8 ms: 1.03x faster                                                    |
| thrift                           | 322 us                                                   | 313 us: 1.03x faster                                                     |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                     |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                     |
| pidigits                         | 161 ms                                                   | 158 ms: 1.02x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.70 ms: 1.02x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.5 ms: 1.01x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 659 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 959 ns: 1.01x faster                                                     |
| bench_thread_pool                | 419 us                                                   | 416 us: 1.01x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.65 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 48.8 ms: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.02x slower                                                     |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.03x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 173 ms: 1.03x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 41.4 ms: 1.04x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 896 us: 1.08x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.82 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.21 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.76 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 124 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 236 ms: 1.11x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.2 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 350 us: 1.79x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.6 ms: 2.51x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                             |

Benchmark hidden because not significant (4): pprint_safe_repr, json, gc_traversal, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251107-3.15.0a1+-d13ee0a/bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.134x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.21x