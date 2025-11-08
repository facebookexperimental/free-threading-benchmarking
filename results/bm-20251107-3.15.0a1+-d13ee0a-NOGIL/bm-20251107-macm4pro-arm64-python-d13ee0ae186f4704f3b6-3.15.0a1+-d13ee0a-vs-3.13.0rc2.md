# Results vs. 3.13.0rc2

- fork: python
- ref: d13ee0ae186f4704f3b6
- machine: darwin-arm64
- commit hash: d13ee0a
- commit date: 2025-11-07
- overall geometric mean: 1.017x faster
- HPT reliability: 53.55%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.09x slower                                                     |
| docutils       | 1.05 sec                                                       | 985 ms: 1.06x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 191 ms: 2.72x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 201 ms: 2.61x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.07x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.86x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 85.0 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.52x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 98.9 ms: 1.44x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.12x faster                                                     |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 48.5 ms: 1.12x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.5 ms: 2.64x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.05x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.6 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.26 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.0 ms: 1.02x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 52.7 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.99 ms: 1.16x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 930 ms: 1.08x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.5 ms: 1.07x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.6 ms: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 149 us: 1.15x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.59 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.99 ms: 1.17x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.15x slower                                                    |
| mako            | 4.41 ms                                                        | 5.61 ms: 1.27x slower                                                    |
| django_template | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 191 ms: 2.72x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 754 us: 2.71x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 201 ms: 2.61x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 468 us: 2.12x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.07x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.86x faster                                                     |
| mdp                              | 1.06 sec                                                       | 603 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 85.0 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.52x faster                                                     |
| k_core                           | 1.46 sec                                                       | 989 ms: 1.48x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 98.9 ms: 1.44x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.30x faster                                                    |
| deepcopy                         | 145 us                                                         | 112 us: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                     |
| go                               | 72.6 ms                                                        | 60.0 ms: 1.21x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.5 ms: 1.17x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.99 ms: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.26 ms: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 193 ms: 1.15x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 825 ns: 1.15x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.12x faster                                                     |
| float                            | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 930 ms: 1.08x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.21 us: 1.07x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 58.5 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.07x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 985 ms: 1.06x faster                                                     |
| pidigits                         | 166 ms                                                         | 159 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.0 ms: 1.02x faster                                                    |
| pycparser                        | 470 ms                                                         | 462 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.03 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| fannkuch                         | 179 ms                                                         | 178 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.03x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| shortest_path                    | 225 ms                                                         | 236 ms: 1.05x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.6 ms: 1.05x slower                                                    |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.3 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.96 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                     |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 346 ms: 1.08x slower                                                     |
| thrift                           | 309 us                                                         | 335 us: 1.08x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.09x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 26.8 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| 2to3                             | 112 ms                                                         | 121 ms: 1.09x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 44.2 ns: 1.09x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.11 ms: 1.09x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 710 ms: 1.09x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 52.7 ms: 1.10x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.60 ms: 1.10x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.59 ms: 1.11x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.2 ms: 1.11x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.49 us: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.5 ms: 1.12x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.77 us: 1.13x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.5 us: 1.14x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 43.3 ms: 1.15x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.15x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.15x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.0 ms: 1.15x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.5 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.7 ms: 1.16x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.99 ms: 1.17x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.18x slower                                                     |
| raytrace                         | 109 ms                                                         | 129 ms: 1.18x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 44.1 ms: 1.19x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.8 ms: 1.19x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.9 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.40 us: 1.23x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.24 ms: 1.26x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.5 ms: 1.26x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.61 ms: 1.27x slower                                                    |
| coverage                         | 31.2 ms                                                        | 39.8 ms: 1.28x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 532 us: 1.29x slower                                                     |
| django_template                  | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.6 ms: 1.35x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 63.5 ms: 1.48x slower                                                    |
| many_optionals                   | 200 us                                                         | 374 us: 1.87x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.5 ms: 2.64x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.7 ms: 2.99x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251107-3.15.0a1+-d13ee0a-NOGIL/bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1+-d13ee0a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.017x faster

# HPT report

- Reliability score: 53.55% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.30x