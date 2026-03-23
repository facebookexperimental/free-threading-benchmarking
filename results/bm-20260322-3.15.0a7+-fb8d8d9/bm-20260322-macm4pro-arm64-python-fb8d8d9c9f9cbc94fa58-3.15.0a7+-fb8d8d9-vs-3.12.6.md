# Results vs. 3.12.6

- fork: python
- ref: fb8d8d9c9f9cbc94fa58
- machine: darwin-arm64
- commit hash: fb8d8d9
- commit date: 2026-03-22
- overall geometric mean: 1.160x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                    |
| sphinx         | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 224 ms: 2.22x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 232 ms: 2.07x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 230 ms: 2.00x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.2 ms: 1.75x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 138 ms: 1.62x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.24x faster                                                     |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.5 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.2 ms: 2.56x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.32x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.0 ms: 1.40x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.5 ms: 1.22x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.19x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.1 ms: 1.18x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.5 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.66 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.6 ms: 1.27x faster                                                    |
| tomli_loads          | 957 ms                                                   | 820 ms: 1.17x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 34.9 ms: 1.11x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.9 ms: 1.06x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                     |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.71 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.27 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.68 ms: 1.08x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.2 ms: 1.03x faster                                                    |
| mako            | 4.77 ms                                                  | 4.76 ms: 1.00x faster                                                    |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.06 ms: 5.12x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 224 ms: 2.22x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 232 ms: 2.07x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.03x faster                                                     |
| mdp                              | 1.09 sec                                                 | 539 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 230 ms: 2.00x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.2 ms: 1.75x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                     |
| deepcopy                         | 161 us                                                   | 97.7 us: 1.65x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 138 ms: 1.62x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.56x faster                                                    |
| float                            | 37.9 ms                                                  | 27.0 ms: 1.40x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.06 us: 1.37x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.20 us: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| go                               | 70.0 ms                                                  | 53.0 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 41.7 ms: 1.30x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.28x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.6 ms: 1.27x faster                                                    |
| k_core                           | 1.12 sec                                                 | 896 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.24x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.5 ms: 1.23x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 116 ms: 1.23x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 41.5 ns: 1.23x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.5 ms: 1.22x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.16 us: 1.19x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 36.6 ms: 1.19x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.1 ms: 1.18x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.6 ms: 1.18x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.38 us: 1.18x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.48 ms: 1.17x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 820 ms: 1.17x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.7 ms: 1.16x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| pyflate                          | 216 ms                                                   | 186 ms: 1.16x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.9 ms: 1.16x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.79 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 44.6 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                    |
| pylint                           | 128 ms                                                   | 114 ms: 1.13x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.5 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.9 ms: 1.11x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.2 us: 1.11x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.75 ms: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| richards                         | 22.4 ms                                                  | 20.6 ms: 1.09x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.4 ms: 1.09x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.68 ms: 1.08x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 464 ms: 1.07x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.50 ms: 1.07x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.9 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                     |
| fannkuch                         | 176 ms                                                   | 169 ms: 1.04x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 96.5 ms: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.9 ms: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.2 ms: 1.03x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 650 ms: 1.02x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 947 ns: 1.02x faster                                                     |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 322 ms: 1.02x faster                                                     |
| thrift                           | 322 us                                                   | 317 us: 1.02x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 38.7 ms: 1.00x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.76 ms: 1.00x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.66 ms: 1.01x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                     |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| connected_components             | 201 ms                                                   | 204 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 425 us: 1.02x slower                                                     |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.06 ms: 1.03x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 173 ms: 1.04x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.7 ms: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.07x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.82 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.71 ms: 1.09x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.27 ms: 1.10x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 915 us: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.0 ms: 1.13x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.1 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.2 ms: 2.56x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |

Benchmark hidden because not significant (1): json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260322-3.15.0a7+-fb8d8d9/bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.160x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.23x