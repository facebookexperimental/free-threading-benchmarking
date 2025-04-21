# Results vs. 3.13.0rc2

- fork: python
- ref: 78cfee6f0920ac914ed1
- machine: darwin-arm64
- commit hash: 78cfee6
- commit date: 2025-04-20
- overall geometric mean: 1.019x faster
- HPT reliability: 55.61%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.01x faster                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.05x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.53x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 43.0 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.0 ms: 3.08x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 49.1 ms: 1.15x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                    |
| regex_dna      | 94.6 ms                                                        | 98.6 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 924 ms: 1.08x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.1 ms: 1.04x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 62.7 ms: 1.01x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 100 us: 1.01x slower                                                     |
| xml_etree_process    | 25.4 ms                                                        | 25.9 ms: 1.02x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.7 ms: 1.02x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.02 ms: 1.08x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.95 ms: 1.04x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.71 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                    |
| mako            | 4.41 ms                                                        | 4.90 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.05x faster                                                     |
| mdp                              | 1.06 sec                                                       | 522 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                     |
| k_core                           | 1.46 sec                                                       | 945 ms: 1.55x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.53x faster                                                     |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.29x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                     |
| go                               | 72.6 ms                                                        | 58.4 ms: 1.24x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.6 ms: 1.24x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.12 us: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.14x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 874 us: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                     |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 924 ms: 1.08x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| float                            | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.1 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| shortest_path                    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| connected_components             | 208 ms                                                         | 203 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.01 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| 2to3                             | 112 ms                                                         | 111 ms: 1.01x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.48 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 43.0 ms: 1.00x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.86 ms: 1.00x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 62.7 ms: 1.01x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 100 us: 1.01x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.1 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 45.2 ms: 1.02x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.9 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 66.0 us: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.7 ms: 1.02x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.03x slower                                                    |
| richards                         | 22.1 ms                                                        | 22.7 ms: 1.03x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 975 ns: 1.03x slower                                                     |
| fannkuch                         | 179 ms                                                         | 185 ms: 1.04x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.95 ms: 1.04x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.6 ms: 1.04x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 335 ms: 1.04x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 98.6 ms: 1.04x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 677 ms: 1.04x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 99.8 ms: 1.05x slower                                                    |
| pycparser                        | 470 ms                                                         | 493 ms: 1.05x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.3 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 40.2 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.8 ms: 1.07x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 133 ms: 1.07x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 443 us: 1.08x slower                                                     |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.39 ms: 1.08x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.56 ms: 1.08x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.02 ms: 1.08x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 47.2 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.44 us: 1.09x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.95 ms: 1.09x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.68 us: 1.09x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.8 ms: 1.10x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.90 ms: 1.11x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.62 us: 1.12x slower                                                    |
| raytrace                         | 109 ms                                                         | 122 ms: 1.12x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.71 ms: 1.13x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.0 ms: 1.13x slower                                                    |
| nbody                            | 42.5 ms                                                        | 49.1 ms: 1.15x slower                                                    |
| many_optionals                   | 200 us                                                         | 233 us: 1.16x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 50.2 ms: 1.17x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.5 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.72 ms: 1.39x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.0 ms: 3.08x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (4): json, pathlib, logging_silent, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250420-3.14.0a7+-78cfee6/bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7+-78cfee6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.019x faster

# HPT report

- Reliability score: 55.61% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.08x