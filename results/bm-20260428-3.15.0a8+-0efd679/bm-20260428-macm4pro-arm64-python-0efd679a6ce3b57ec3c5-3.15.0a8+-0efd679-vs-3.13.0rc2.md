# Results vs. 3.13.0rc2

- fork: python
- ref: 0efd679a6ce3b57ec3c5
- machine: darwin-arm64
- commit hash: 0efd679
- commit date: 2026-04-28
- overall geometric mean: 1.089x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                    |
| sphinx         | 409 ms                                                         | 395 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 220 ms: 2.38x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 229 ms: 1.69x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.0 ms: 1.35x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.11x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 234 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.5 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.8 ms: 1.13x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.1 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.79 ms: 1.09x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.6 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 823 ms: 1.21x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.0 ms: 1.13x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 96.7 us: 1.03x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 65.9 ms: 1.06x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 5.85 ms: 1.02x faster                                                    |
| python_startup         | 8.63 ms                                                        | 8.57 ms: 1.01x faster                                                    |
| Geometric mean         | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.53 ms: 1.05x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.9 ms: 1.02x faster                                                    |
| mako            | 4.41 ms                                                        | 4.79 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 14.8 ms: 1.19x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 220 ms: 2.38x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                     |
| pylint                           | 106 ms                                                         | 50.7 ms: 2.08x faster                                                    |
| mdp                              | 1.06 sec                                                       | 536 ms: 1.98x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 229 ms: 1.69x faster                                                     |
| k_core                           | 1.46 sec                                                       | 898 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.99 ms: 1.57x faster                                                    |
| deepcopy                         | 145 us                                                         | 97.5 us: 1.49x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.44x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| go                               | 72.6 ms                                                        | 52.5 ms: 1.38x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.0 ms: 1.35x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.8 ms: 1.29x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                    |
| pyflate                          | 222 ms                                                         | 182 ms: 1.22x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 823 ms: 1.21x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| float                            | 31.4 ms                                                        | 27.8 ms: 1.13x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.0 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.12x faster                                                   |
| async_generators                 | 193 ms                                                         | 175 ms: 1.11x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.79 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.79 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.7 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.7 ms: 1.07x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 933 us: 1.06x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.06x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.06x faster                                                     |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.5 ms: 1.05x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 45.6 ms: 1.05x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 35.6 ms: 1.05x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 307 ms: 1.05x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.53 ms: 1.05x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 622 ms: 1.04x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.73 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| sphinx                           | 409 ms                                                         | 395 ms: 1.04x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 96.7 us: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 20.9 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 42.9 ms: 1.02x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                    |
| connected_components             | 208 ms                                                         | 204 ms: 1.02x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 5.85 ms: 1.02x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.6 us: 1.02x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 464 ms: 1.01x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.44 ms: 1.01x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.57 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 942 ns: 1.01x faster                                                     |
| deltablue                        | 1.45 ms                                                        | 1.45 ms: 1.00x faster                                                    |
| thrift                           | 309 us                                                         | 317 us: 1.02x slower                                                     |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.00 us: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 427 us: 1.04x slower                                                     |
| nbody                            | 42.5 ms                                                        | 44.1 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.7 ms: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 115 ms: 1.05x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.05x slower                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 65.9 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.3 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 171 ms: 1.07x slower                                                     |
| coverage                         | 31.2 ms                                                        | 33.5 ms: 1.07x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 46.2 ms: 1.08x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.79 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 234 ms: 1.13x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 38.5 ms: 1.15x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.0 ms: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.8 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.9 ms: 1.19x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.49 ms: 1.22x slower                                                    |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.5 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (5): logging_format, chaos, scimark_sparse_mat_mult, regex_dna, logging_silent
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260428-3.15.0a8+-0efd679/bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.089x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.19x