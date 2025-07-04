# Results vs. 3.13.0rc2

- fork: python
- ref: b4991056f4f44acb50ae
- machine: darwin-arm64
- commit hash: b499105
- commit date: 2025-07-03
- overall geometric mean: 1.019x faster
- HPT reliability: 76.31%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.10x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.1 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 231 ms: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.5 ms: 1.15x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.1 ms: 2.73x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                   |
| pidigits       | 166 ms                                                         | 166 ms: 1.00x slower                                                    |
| nbody          | 42.5 ms                                                        | 54.9 ms: 1.29x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.5 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.2 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.0 ms: 1.21x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.4 ms: 1.07x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 971 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.6 ms: 1.02x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.6 ms: 1.05x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.62 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.99 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.4 ms: 1.09x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.13x slower                                                   |
| mako            | 4.41 ms                                                        | 5.60 ms: 1.27x slower                                                   |
| django_template | 12.5 ms                                                        | 16.0 ms: 1.28x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.68x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 789 us: 2.59x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 491 us: 2.02x faster                                                    |
| mdp                              | 1.06 sec                                                       | 574 ms: 1.84x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.1 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 991 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.0 ms: 1.21x faster                                                   |
| deepcopy                         | 145 us                                                         | 120 us: 1.21x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                    |
| go                               | 72.6 ms                                                        | 61.0 ms: 1.19x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 14.0 us: 1.18x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.1 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 817 ns: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 58.4 ms: 1.07x faster                                                   |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 971 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.26 us: 1.02x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.00x faster                                                   |
| pidigits                         | 166 ms                                                         | 166 ms: 1.00x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| dask                             | 525 ms                                                         | 530 ms: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.6 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.5 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| json                             | 1.94 ms                                                        | 2.02 ms: 1.04x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.22 ms: 1.05x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.6 ms: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 221 ms: 1.06x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.02 ms: 1.06x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.5 ms: 1.07x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.06 ms: 1.07x slower                                                   |
| thrift                           | 309 us                                                         | 331 us: 1.07x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 346 ms: 1.07x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 705 ms: 1.09x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.2 ms: 1.09x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 26.9 ms: 1.09x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.4 ms: 1.09x slower                                                   |
| 2to3                             | 112 ms                                                         | 122 ms: 1.10x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 231 ms: 1.11x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.62 ms: 1.11x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 45.5 ns: 1.12x slower                                                   |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 139 ms: 1.12x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 72.9 us: 1.13x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 42.1 ms: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.9 ms: 1.13x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 54.5 ms: 1.14x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.5 ms: 1.15x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.88 us: 1.16x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.59 us: 1.16x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.9 ms: 1.16x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.99 ms: 1.17x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.18x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.8 ms: 1.18x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.90 us: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.2 ms: 1.19x slower                                                   |
| raytrace                         | 109 ms                                                         | 131 ms: 1.20x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.4 ms: 1.21x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.3 ms: 1.23x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.22 ms: 1.25x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.0 ms: 1.25x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.60 ms: 1.27x slower                                                   |
| many_optionals                   | 200 us                                                         | 257 us: 1.28x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.0 ms: 1.28x slower                                                   |
| nbody                            | 42.5 ms                                                        | 54.9 ms: 1.29x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 55.9 ms: 1.31x slower                                                   |
| coverage                         | 31.2 ms                                                        | 41.0 ms: 1.32x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 584 us: 1.42x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.80 ms: 1.57x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.1 ms: 2.73x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (4): json_dumps, fannkuch, pycparser, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250703-3.15.0a0-b499105-NOGIL/bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.019x faster

# HPT report

- Reliability score: 76.31% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x