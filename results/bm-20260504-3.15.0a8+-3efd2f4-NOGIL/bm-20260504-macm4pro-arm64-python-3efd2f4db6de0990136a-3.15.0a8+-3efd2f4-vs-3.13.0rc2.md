# Results vs. 3.13.0rc2

- fork: python
- ref: 3efd2f4db6de0990136a
- machine: darwin-arm64
- commit hash: 3efd2f4
- commit date: 2026-05-04
- overall geometric mean: 1.026x faster
- HPT reliability: 78.78%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 999 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 422 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 243 ms: 2.15x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.13x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 190 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.6 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.5 ms: 3.27x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.9 ms: 1.36x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.22 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 52.6 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.96 ms: 1.17x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.7 ms: 1.13x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 888 ms: 1.13x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.3 ms: 1.07x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.03x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 38.1 ms: 1.06x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.5 ms: 1.08x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 149 us: 1.15x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 12.5 ms                                                        | 16.1 ms: 1.29x slower                                                    |
| mako            | 4.41 ms                                                        | 5.74 ms: 1.30x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.29x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 809 us: 2.52x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 243 ms: 2.15x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.13x faster                                                     |
| pylint                           | 106 ms                                                         | 51.7 ms: 2.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 516 us: 1.92x faster                                                     |
| mdp                              | 1.06 sec                                                       | 603 ms: 1.75x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.12 ms: 1.52x faster                                                    |
| k_core                           | 1.46 sec                                                       | 985 ms: 1.49x faster                                                     |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| go                               | 72.6 ms                                                        | 59.7 ms: 1.21x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 802 ns: 1.18x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.96 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.22 ms: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.9 ms: 1.15x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.7 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 888 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| float                            | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.21 us: 1.07x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 58.3 ms: 1.07x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| docutils                         | 1.05 sec                                                       | 999 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| async_generators                 | 193 ms                                                         | 190 ms: 1.02x faster                                                     |
| pycparser                        | 470 ms                                                         | 463 ms: 1.02x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.04 ms: 1.01x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.01x slower                                                     |
| sphinx                           | 409 ms                                                         | 422 ms: 1.03x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 339 ms: 1.05x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 688 ms: 1.06x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 38.1 ms: 1.06x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.6 ms: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.10 ms: 1.08x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.42 us: 1.08x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.5 ms: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.2 ns: 1.09x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.0 ms: 1.09x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.68 us: 1.10x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.8 ms: 1.10x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.6 ms: 1.10x slower                                                    |
| shortest_path                    | 225 ms                                                         | 248 ms: 1.10x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.6 ms: 1.10x slower                                                    |
| thrift                           | 309 us                                                         | 344 us: 1.11x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 41.6 ms: 1.12x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.12x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.22 ms: 1.13x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.2 us: 1.13x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.7 ms: 1.14x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.15x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 50.7 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.9 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.2 ms: 1.17x slower                                                    |
| connected_components             | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| raytrace                         | 109 ms                                                         | 128 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.18x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.15 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.24 us: 1.21x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.4 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| coverage                         | 31.2 ms                                                        | 39.7 ms: 1.27x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.1 ms: 1.29x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.74 ms: 1.30x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 44.1 ms: 1.31x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.8 ms: 1.33x slower                                                    |
| many_optionals                   | 200 us                                                         | 271 us: 1.35x slower                                                     |
| nbody                            | 42.5 ms                                                        | 57.9 ms: 1.36x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 567 us: 1.38x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 59.0 ms: 1.38x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.5 ms: 3.27x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (4): regex_dna, dask, async_tree_eager_cpu_io_mixed, fannkuch
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260504-3.15.0a8+-3efd2f4-NOGIL/bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.026x faster

# HPT report

- Reliability score: 78.78% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.32x