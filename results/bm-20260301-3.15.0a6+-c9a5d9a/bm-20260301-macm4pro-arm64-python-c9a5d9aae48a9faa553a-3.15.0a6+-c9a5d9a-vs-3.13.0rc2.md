# Results vs. 3.13.0rc2

- fork: python
- ref: c9a5d9aae48a9faa553a
- machine: darwin-arm64
- commit hash: c9a5d9a
- commit date: 2026-03-01
- overall geometric mean: 1.085x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.3 ms: 1.09x faster                                                    |
| sphinx         | 409 ms                                                         | 390 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 217 ms: 2.40x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 223 ms: 2.36x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 231 ms: 1.67x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.3 ms: 1.43x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.1 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| async_generators                 | 193 ms                                                         | 173 ms: 1.11x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.0 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.97 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.9 ms: 2.80x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.9 ms: 1.17x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 46.1 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.3 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|---------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps          | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                    |
| tomli_loads         | 1000 ms                                                        | 830 ms: 1.20x faster                                                     |
| xml_etree_iterparse | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| xml_etree_generate  | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| xml_etree_process   | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                    |
| json_loads          | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| xml_etree_parse     | 62.4 ms                                                        | 63.2 ms: 1.01x slower                                                    |
| pickle_pure_python  | 130 us                                                         | 139 us: 1.06x slower                                                     |
| Geometric mean      | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.81 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.57 ms: 1.04x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| mako            | 4.41 ms                                                        | 4.67 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 217 ms: 2.40x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 223 ms: 2.36x faster                                                     |
| mdp                              | 1.06 sec                                                       | 537 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 231 ms: 1.67x faster                                                     |
| k_core                           | 1.46 sec                                                       | 893 ms: 1.64x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.99 ms: 1.57x faster                                                    |
| deepcopy                         | 145 us                                                         | 96.7 us: 1.50x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.44x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.3 ms: 1.43x faster                                                    |
| go                               | 72.6 ms                                                        | 51.9 ms: 1.40x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.1 ms: 1.35x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 830 ms: 1.20x faster                                                     |
| pyflate                          | 222 ms                                                         | 186 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| float                            | 31.4 ms                                                        | 26.9 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| richards                         | 22.1 ms                                                        | 19.7 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.11x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.2 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 908 us: 1.09x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 21.3 ms: 1.09x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.83 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.7 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.0 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.97 ms: 1.08x faster                                                    |
| fannkuch                         | 179 ms                                                         | 166 ms: 1.07x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 117 ms: 1.05x faster                                                     |
| sphinx                           | 409 ms                                                         | 390 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.57 ms: 1.04x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.74 ms: 1.04x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.3 ms: 1.03x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.17 us: 1.03x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.38 us: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| pycparser                        | 470 ms                                                         | 460 ms: 1.02x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 637 ms: 1.02x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 316 ms: 1.02x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 43.2 ms: 1.01x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 64.1 us: 1.01x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.44 ms: 1.01x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.47 ms: 1.01x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.03 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| chaos                            | 24.3 ms                                                        | 24.2 ms: 1.00x faster                                                    |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.00x slower                                                     |
| connected_components             | 208 ms                                                         | 209 ms: 1.00x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.79 ms: 1.01x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.2 ms: 1.01x slower                                                    |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 6.90 us: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.81 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.9 ms: 1.02x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.2 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.1 ms: 1.03x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.04x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 44.9 ms: 1.05x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.67 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.5 ms: 1.06x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.06x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| nbody                            | 42.5 ms                                                        | 46.1 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.4 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.9 ms: 1.19x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.7 ms: 1.19x slower                                                    |
| many_optionals                   | 200 us                                                         | 248 us: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.9 ms: 2.80x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (5): thrift, sqlite_synth, regex_dna, unpickle_pure_python, logging_silent
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260301-3.15.0a6+-c9a5d9a/bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.085x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.19x