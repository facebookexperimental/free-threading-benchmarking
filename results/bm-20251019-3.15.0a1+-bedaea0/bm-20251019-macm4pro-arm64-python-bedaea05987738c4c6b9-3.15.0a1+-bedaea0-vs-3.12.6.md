# Results vs. 3.12.6

- fork: python
- ref: bedaea05987738c4c6b9
- machine: darwin-arm64
- commit hash: bedaea0
- commit date: 2025-10-19
- overall geometric mean: 1.104x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                    |
| sphinx         | 434 ms                                                   | 407 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 244 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.84x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 249 ms: 1.79x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.60x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 260 ms: 1.28x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| async_generators                 | 206 ms                                                   | 174 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.2 ms: 1.10x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.2 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                    |
| nbody          | 54.2 ms                                                  | 49.1 ms: 1.11x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.12x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 48.9 ms: 1.12x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.0 ms: 1.20x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.9 ms: 1.12x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.5 ms: 1.10x faster                                                    |
| tomli_loads          | 957 ms                                                   | 903 ms: 1.06x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                     |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.03x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.86 ms: 1.10x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.34 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.97 ms: 1.05x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 22.1 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.13x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 244 ms: 2.03x faster                                                     |
| mdp                              | 1.09 sec                                                 | 542 ms: 2.01x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.84x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 249 ms: 1.79x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.60x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.0 us: 1.52x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                     |
| deepcopy                         | 161 us                                                   | 109 us: 1.48x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.45 us: 1.32x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 260 ms: 1.28x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                    |
| float                            | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                    |
| go                               | 70.0 ms                                                  | 56.2 ms: 1.25x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.1 ms: 1.23x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.9 ms: 1.22x faster                                                    |
| raytrace                         | 145 ms                                                   | 119 ms: 1.22x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 42.4 ns: 1.20x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.0 ms: 1.20x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 51.3 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 174 ms: 1.18x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.6 ms: 1.18x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.8 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                   |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.52 ms: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 989 ms: 1.13x faster                                                     |
| pylint                           | 128 ms                                                   | 113 ms: 1.13x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 63.3 us: 1.12x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.9 ms: 1.12x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.9 ms: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.1 ms: 1.11x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.1 ms: 1.11x faster                                                    |
| nbody                            | 54.2 ms                                                  | 49.1 ms: 1.11x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.2 ms: 1.10x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.10x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.5 ms: 1.10x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.90 ms: 1.09x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.36 us: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.38 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.7 ms: 1.09x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.59 us: 1.08x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.85 ms: 1.07x faster                                                    |
| sphinx                           | 434 ms                                                   | 407 ms: 1.07x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 903 ms: 1.06x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.97 ms: 1.05x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 49.0 ms: 1.05x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.2 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 24.5 ms: 1.04x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.6 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.7 ms: 1.03x faster                                                    |
| thrift                           | 322 us                                                   | 312 us: 1.03x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                     |
| pycparser                        | 497 ms                                                   | 484 ms: 1.03x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 946 ns: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                     |
| bench_thread_pool                | 419 us                                                   | 413 us: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 659 ms: 1.01x faster                                                     |
| json                             | 1.93 ms                                                  | 1.92 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 162 ms: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.1 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.05 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                     |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.02x slower                                                     |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.2 ms: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.03x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 42.4 ms: 1.07x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.87 ms: 1.10x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.86 ms: 1.10x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.34 ms: 1.11x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 934 us: 1.13x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                    |
| many_optionals                   | 195 us                                                   | 365 us: 1.87x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.2 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (3): pprint_safe_repr, json_loads, mako
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251019-3.15.0a1+-bedaea0/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.104x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.19x