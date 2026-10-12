# Results vs. 3.13.0rc2

- fork: python
- ref: aab474a35b7d47aa3404
- machine: darwin-arm64
- commit hash: aab474a
- commit date: 2026-10-11
- overall geometric mean: 1.097x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| docutils       | 1.05 sec                                                       | 904 ms: 1.16x faster                                                    |
| html5lib       | 23.1 ms                                                        | 20.7 ms: 1.12x faster                                                   |
| sphinx         | 409 ms                                                         | 388 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                          | 1.07x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 264 ms: 1.99x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 277 ms: 1.88x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 281 ms: 1.44x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 272 ms: 1.42x faster                                                    |
| async_generators                 | 193 ms                                                         | 142 ms: 1.36x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.28x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.19x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 158 ms: 1.18x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 162 ms: 1.14x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.75 ms: 1.10x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 275 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.1 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.38x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.6 ms: 3.24x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                   |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.23 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 91.3 ms: 1.04x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 54.4 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.60 ms: 1.29x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 827 ms: 1.21x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.5 ms: 1.11x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 92.1 us: 1.08x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 34.9 ms: 1.03x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.3 ms: 1.01x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 136 us: 1.04x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.85 ms: 1.02x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.46 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.46 ms: 1.01x slower                                                   |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 503 ms: 2.10x faster                                                    |
| pylint                           | 106 ms                                                         | 52.4 ms: 2.01x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 264 ms: 1.99x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 277 ms: 1.88x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 635 us: 1.57x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.00 ms: 1.56x faster                                                   |
| deepcopy                         | 145 us                                                         | 96.1 us: 1.51x faster                                                   |
| k_core                           | 1.46 sec                                                       | 972 ms: 1.50x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 281 ms: 1.44x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 272 ms: 1.42x faster                                                    |
| go                               | 72.6 ms                                                        | 51.5 ms: 1.41x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.39x faster                                                   |
| async_generators                 | 193 ms                                                         | 142 ms: 1.36x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 48.5 us: 1.33x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 48.6 ms: 1.32x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.60 ms: 1.29x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                                   |
| pyflate                          | 222 ms                                                         | 177 ms: 1.25x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 827 ms: 1.21x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.19x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 158 ms: 1.18x faster                                                    |
| float                            | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.23 ms: 1.16x faster                                                   |
| docutils                         | 1.05 sec                                                       | 904 ms: 1.16x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 1.77 ms: 1.15x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 162 ms: 1.14x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 20.7 ms: 1.12x faster                                                   |
| fannkuch                         | 179 ms                                                         | 160 ms: 1.11x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 111 ms: 1.11x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.5 ms: 1.11x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                  |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.0 ms: 1.11x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.75 ms: 1.10x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.1 ms: 1.10x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 275 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.63 ms: 1.08x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.8 ms: 1.08x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 92.1 us: 1.08x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 34.6 ms: 1.08x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 40.9 ms: 1.07x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.88 ms: 1.06x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                   |
| sphinx                           | 409 ms                                                         | 388 ms: 1.05x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.1 ms: 1.05x faster                                                   |
| json                             | 1.94 ms                                                        | 1.85 ms: 1.05x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.34 us: 1.04x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.56 us: 1.04x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 91.3 ms: 1.04x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 917 ns: 1.03x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 312 ms: 1.03x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.9 ms: 1.03x faster                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.73 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.36 ms: 1.02x faster                                                   |
| thrift                           | 309 us                                                         | 303 us: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.44 ms: 1.01x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 645 ms: 1.01x faster                                                    |
| bench_thread_pool                | 412 us                                                         | 409 us: 1.01x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.2 ms: 1.01x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.46 ms: 1.01x slower                                                   |
| chaos                            | 24.3 ms                                                        | 24.6 ms: 1.01x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 63.3 ms: 1.01x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.85 ms: 1.02x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 98.9 ms: 1.04x slower                                                   |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 136 us: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.04x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.9 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.0 ms: 1.05x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.0 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.46 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 36.9 ms: 1.10x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.4 ms: 1.13x slower                                                   |
| many_optionals                   | 200 us                                                         | 229 us: 1.14x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.2 ms: 1.17x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.38x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.6 ms: 3.24x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.09x faster                                                            |

Benchmark hidden because not significant (5): pycparser, shortest_path, nbody, connected_components, logging_silent
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261011-3.16.0a0-aab474a/bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.097x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x