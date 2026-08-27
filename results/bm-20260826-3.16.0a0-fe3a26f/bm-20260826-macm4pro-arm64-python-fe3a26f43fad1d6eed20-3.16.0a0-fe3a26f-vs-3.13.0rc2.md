# Results vs. 3.13.0rc2

- fork: python
- ref: fe3a26f43fad1d6eed20
- machine: darwin-arm64
- commit hash: fe3a26f
- commit date: 2026-08-26
- overall geometric mean: 1.053x faster
- HPT reliability: 99.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.06x slower                                                    |
| docutils       | 1.05 sec                                                       | 950 ms: 1.10x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.3 ms: 1.09x faster                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 310 ms: 1.70x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 334 ms: 1.56x faster                                                    |
| async_generators                 | 193 ms                                                         | 145 ms: 1.33x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 314 ms: 1.23x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 331 ms: 1.23x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 121 ms: 1.17x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.86 ms: 1.09x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 126 ms: 1.05x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.05x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.4 ms: 1.04x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 177 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 283 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 292 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 227 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 263 ms: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 153 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.57x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| pidigits       | 166 ms                                                         | 166 ms: 1.00x faster                                                    |
| nbody          | 42.5 ms                                                        | 43.1 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.21 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 91.7 ms: 1.03x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 54.8 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.60 ms: 1.29x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 804 ms: 1.24x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.8 ms: 1.05x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 97.9 us: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.6 ms: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.09x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 68.1 ms: 1.09x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.18 ms: 1.06x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.68 ms: 1.12x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.66 ms: 1.06x slower                                                   |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 521 ms: 2.03x faster                                                    |
| pylint                           | 106 ms                                                         | 56.8 ms: 1.86x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 310 ms: 1.70x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 334 ms: 1.56x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.09 ms: 1.53x faster                                                   |
| deepcopy                         | 145 us                                                         | 97.1 us: 1.49x faster                                                   |
| k_core                           | 1.46 sec                                                       | 981 ms: 1.49x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                   |
| go                               | 72.6 ms                                                        | 53.9 ms: 1.35x faster                                                   |
| async_generators                 | 193 ms                                                         | 145 ms: 1.33x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 49.3 us: 1.31x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.60 ms: 1.29x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.8 ms: 1.29x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 804 ms: 1.24x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 314 ms: 1.23x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 331 ms: 1.23x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.22x faster                                                   |
| pyflate                          | 222 ms                                                         | 184 ms: 1.20x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 826 us: 1.20x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 121 ms: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.21 ms: 1.16x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                   |
| fannkuch                         | 179 ms                                                         | 160 ms: 1.11x faster                                                    |
| docutils                         | 1.05 sec                                                       | 950 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 9.86 ms: 1.09x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.3 ms: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.08x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.4 ms: 1.08x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.07x faster                                                    |
| float                            | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.07x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.0 ms: 1.07x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.2 ms: 1.06x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.93 ms: 1.06x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.90 ms: 1.06x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 126 ms: 1.05x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.8 ms: 1.05x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.05x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 35.5 ms: 1.05x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 41.8 ms: 1.05x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.73 ms: 1.04x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.4 ms: 1.04x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 309 ms: 1.04x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 177 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 283 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 292 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 91.7 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 635 ms: 1.02x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 97.9 us: 1.02x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.21 us: 1.01x faster                                                   |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.73 us: 1.01x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 937 ns: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.49 ms: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 166 ms: 1.00x faster                                                    |
| connected_components             | 208 ms                                                         | 209 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 227 ms: 1.01x slower                                                    |
| nbody                            | 42.5 ms                                                        | 43.1 ms: 1.01x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                   |
| thrift                           | 309 us                                                         | 315 us: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.4 ns: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.6 ms: 1.02x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 422 us: 1.02x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.82 ms: 1.03x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 100.0 ms: 1.05x slower                                                  |
| pycparser                        | 470 ms                                                         | 494 ms: 1.05x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.5 ms: 1.05x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.66 ms: 1.06x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| 2to3                             | 112 ms                                                         | 119 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.6 ms: 1.06x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.18 ms: 1.06x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.09x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 68.1 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.6 ms: 1.12x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.68 ms: 1.12x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.9 ms: 1.14x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.8 ms: 1.14x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 49.7 ms: 1.16x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.9 ms: 1.19x slower                                                   |
| many_optionals                   | 200 us                                                         | 239 us: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 263 ms: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 153 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.57x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (4): sphinx, logging_format, shortest_path, json_loads
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260826-3.16.0a0-fe3a26f/bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.053x faster

# HPT report

- Reliability score: 99.52% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x