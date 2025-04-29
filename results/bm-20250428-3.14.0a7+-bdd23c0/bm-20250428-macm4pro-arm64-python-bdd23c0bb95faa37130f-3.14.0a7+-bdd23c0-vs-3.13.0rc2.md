# Results vs. 3.13.0rc2

- fork: python
- ref: bdd23c0bb95faa37130f
- machine: darwin-arm64
- commit hash: bdd23c0
- commit date: 2025-04-28
- overall geometric mean: 1.034x faster
- HPT reliability: 92.72%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                    |
| sphinx         | 409 ms                                                         | 404 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.14x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 249 ms: 2.09x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 249 ms: 1.55x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.27x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                     |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 271 ms: 1.11x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.5 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 258 ms: 1.24x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.5 ms: 3.02x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 48.0 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 99.0 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 918 ms: 1.09x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.7 ms: 1.05x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 98.6 us: 1.01x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.3 ms: 1.01x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 4.95 ms: 1.07x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 144 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 6.04 ms: 1.02x slower                                                    |
| python_startup         | 8.63 ms                                                        | 8.77 ms: 1.02x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.88 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.89 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.14x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 249 ms: 2.09x faster                                                     |
| mdp                              | 1.06 sec                                                       | 510 ms: 2.07x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                     |
| k_core                           | 1.46 sec                                                       | 940 ms: 1.56x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 249 ms: 1.55x faster                                                     |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.7 ms: 1.29x faster                                                    |
| go                               | 72.6 ms                                                        | 57.0 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.27x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.11 us: 1.17x faster                                                    |
| pyflate                          | 222 ms                                                         | 196 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 888 us: 1.12x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 271 ms: 1.11x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                     |
| float                            | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 918 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.7 ms: 1.05x faster                                                    |
| shortest_path                    | 225 ms                                                         | 215 ms: 1.05x faster                                                     |
| connected_components             | 208 ms                                                         | 199 ms: 1.04x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.97 ms: 1.03x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.29 ms: 1.03x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 24.0 ms: 1.03x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.1 ms: 1.03x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.5 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.79 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.5 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                     |
| sphinx                           | 409 ms                                                         | 404 ms: 1.01x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 64.0 us: 1.01x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.88 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.6 us: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 941 ns: 1.01x faster                                                     |
| fannkuch                         | 179 ms                                                         | 178 ms: 1.01x faster                                                     |
| nqueens                          | 37.2 ms                                                        | 37.7 ms: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.3 ms: 1.01x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.04 ms: 1.02x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.77 ms: 1.02x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 97.1 ms: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.3 ns: 1.02x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 163 ms: 1.02x slower                                                     |
| pycparser                        | 470 ms                                                         | 483 ms: 1.03x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 332 ms: 1.03x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 45.2 ms: 1.03x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.03x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 673 ms: 1.04x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.51 ms: 1.04x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 99.0 ms: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 54.8 ms: 1.05x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.25 ms: 1.05x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.59 us: 1.06x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 40.3 ms: 1.06x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.95 ms: 1.07x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 440 us: 1.07x slower                                                     |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.08x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.7 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.93 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 36.8 ms: 1.10x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.11x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.89 ms: 1.11x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.63 us: 1.12x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 48.2 ms: 1.13x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.7 ms: 1.13x slower                                                    |
| nbody                            | 42.5 ms                                                        | 48.0 ms: 1.13x slower                                                    |
| many_optionals                   | 200 us                                                         | 233 us: 1.16x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 258 ms: 1.24x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.75 ms: 1.40x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.5 ms: 3.02x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (8): gc_traversal, xml_etree_parse, 2to3, sqlalchemy_declarative, genshi_xml, regex_compile, xml_etree_process, json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.034x faster

# HPT report

- Reliability score: 92.72% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.08x