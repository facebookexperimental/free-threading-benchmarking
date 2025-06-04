# Results vs. 3.13.0rc2

- fork: python
- ref: b525e31b7fc50e7a498f
- machine: darwin-arm64
- commit hash: b525e31
- commit date: 2025-06-03
- overall geometric mean: 1.019x faster
- HPT reliability: 59.61%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.08x slower                                                    |
| docutils       | 1.05 sec                                                       | 995 ms: 1.05x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.58x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.4 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.9 ms: 1.13x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.7 ms: 2.69x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.9 ms: 1.13x faster                                                   |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 54.3 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.20 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.9 ms: 1.01x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.1 ms: 1.18x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.2 ms: 1.07x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 972 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.04x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.11x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.42 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.88 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.4 ms: 1.09x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                   |
| mako            | 4.41 ms                                                        | 5.75 ms: 1.30x slower                                                   |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.33x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 768 us: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.58x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 480 us: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| mdp                              | 1.06 sec                                                       | 557 ms: 1.90x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.4 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 988 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| deepcopy                         | 145 us                                                         | 119 us: 1.22x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.8 us: 1.20x faster                                                   |
| go                               | 72.6 ms                                                        | 60.7 ms: 1.20x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.1 ms: 1.18x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.20 ms: 1.16x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.3 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 829 ns: 1.14x faster                                                    |
| float                            | 31.4 ms                                                        | 27.9 ms: 1.13x faster                                                   |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                  |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 58.2 ms: 1.07x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                   |
| docutils                         | 1.05 sec                                                       | 995 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 972 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.01x faster                                                   |
| pycparser                        | 470 ms                                                         | 467 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 95.9 ms: 1.01x slower                                                   |
| fannkuch                         | 179 ms                                                         | 184 ms: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.04x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.88 ms: 1.05x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 2.98 ms: 1.05x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.26 ms: 1.06x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                   |
| thrift                           | 309 us                                                         | 330 us: 1.07x slower                                                    |
| connected_components             | 208 ms                                                         | 222 ms: 1.07x slower                                                    |
| 2to3                             | 112 ms                                                         | 120 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.42 ms: 1.09x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 40.7 ms: 1.09x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.4 ms: 1.09x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 52.7 ms: 1.10x slower                                                   |
| richards                         | 22.1 ms                                                        | 24.3 ms: 1.10x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                   |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.11x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.4 ms: 1.12x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.7 ms: 1.12x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.12x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 139 ms: 1.13x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 72.9 us: 1.13x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 48.9 ms: 1.13x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 108 ms: 1.13x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 59.7 ms: 1.14x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.88 ms: 1.16x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.87 us: 1.16x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.16x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 186 ms: 1.17x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 376 ms: 1.17x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.4 ms: 1.17x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.4 ms: 1.17x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 768 ms: 1.18x slower                                                    |
| raytrace                         | 109 ms                                                         | 130 ms: 1.19x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.9 ms: 1.20x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.3 ms: 1.21x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.15 ms: 1.21x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.2 ms: 1.25x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.81 us: 1.26x slower                                                   |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                    |
| logging_format                   | 2.45 us                                                        | 3.10 us: 1.27x slower                                                   |
| nbody                            | 42.5 ms                                                        | 54.3 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.9 ms: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.75 ms: 1.30x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.33x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 595 us: 1.45x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 66.1 ms: 1.55x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 9.75 ms: 1.56x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.7 ms: 2.69x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 217 ns: 5.35x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (2): json_dumps, sphinx
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250603-3.15.0a0-b525e31-NOGIL/bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.019x faster

# HPT report

- Reliability score: 59.61% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x