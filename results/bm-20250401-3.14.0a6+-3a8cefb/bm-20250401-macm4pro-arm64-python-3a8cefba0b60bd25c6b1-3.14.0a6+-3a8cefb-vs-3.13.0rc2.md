# Results vs. 3.13.0rc2

- fork: python
- ref: 3a8cefba0b60bd25c6b1
- machine: darwin-arm64
- commit hash: 3a8cefb
- commit date: 2025-04-01
- overall geometric mean: 1.024x faster
- HPT reliability: 78.43%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.01x faster                                                     |
| html5lib       | 23.1 ms                                                        | 21.9 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.08x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 254 ms: 1.59x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 267 ms: 1.45x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.30x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 259 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 42.0 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 133 ms: 1.30x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.3 ms: 3.05x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                    |
| pidigits       | 166 ms                                                         | 160 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 47.7 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.92 ms: 1.08x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 92.6 ms: 1.02x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 47.1 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 833 ms: 1.20x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 36.0 ms: 1.01x slower                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 46.9 ms: 1.02x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 64.0 ms: 1.03x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 102 us: 1.03x slower                                                     |
| xml_etree_process    | 25.4 ms                                                        | 26.1 ms: 1.03x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 4.96 ms: 1.07x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.44 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 20.7 ms: 1.03x faster                                                    |
| genshi_text     | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                    |
| mako            | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.08x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.03x faster                                                     |
| mdp                              | 1.06 sec                                                       | 543 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 254 ms: 1.59x faster                                                     |
| k_core                           | 1.46 sec                                                       | 959 ms: 1.53x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 267 ms: 1.45x faster                                                     |
| deepcopy                         | 145 us                                                         | 107 us: 1.36x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.2 us: 1.35x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.30x faster                                                     |
| go                               | 72.6 ms                                                        | 56.1 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 833 ms: 1.20x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 53.7 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.12 us: 1.15x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.2 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 259 ms: 1.14x faster                                                     |
| pyflate                          | 222 ms                                                         | 196 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 895 us: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.92 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.9 ms: 1.05x faster                                                    |
| float                            | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.2 ms: 1.04x faster                                                    |
| pidigits                         | 166 ms                                                         | 160 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 20.7 ms: 1.03x faster                                                    |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 42.0 ms: 1.03x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 24.0 ms: 1.03x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 92.6 ms: 1.02x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 47.1 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                     |
| 2to3                             | 112 ms                                                         | 110 ms: 1.01x faster                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 37.4 ms: 1.01x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.0 ms: 1.01x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 44.7 ms: 1.01x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.12 ms: 1.02x slower                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 46.9 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                    |
| fannkuch                         | 179 ms                                                         | 182 ms: 1.02x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.5 ms: 1.02x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.4 ms: 1.02x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.69 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 66.2 us: 1.02x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.6 ns: 1.02x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 666 ms: 1.03x slower                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 64.0 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 102 us: 1.03x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.1 ms: 1.03x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.1 ms: 1.03x slower                                                    |
| pycparser                        | 470 ms                                                         | 486 ms: 1.03x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 333 ms: 1.03x slower                                                     |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.19 ms: 1.04x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.55 us: 1.04x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.33 us: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 431 us: 1.05x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.54 ms: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.8 ms: 1.07x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.96 ms: 1.07x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 172 ms: 1.08x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.44 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.93 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                     |
| generators                       | 15.7 ms                                                        | 17.3 ms: 1.10x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.54 us: 1.11x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 137 ms: 1.11x slower                                                     |
| chaos                            | 24.3 ms                                                        | 26.9 ms: 1.11x slower                                                    |
| raytrace                         | 109 ms                                                         | 121 ms: 1.11x slower                                                     |
| nbody                            | 42.5 ms                                                        | 47.7 ms: 1.12x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 42.2 ms: 1.13x slower                                                    |
| many_optionals                   | 200 us                                                         | 229 us: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 39.4 ms: 1.17x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.4 ms: 1.17x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 52.4 ms: 1.23x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 133 ms: 1.30x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.56 ms: 1.37x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.3 ms: 3.05x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (5): json, sqlite_synth, hexiom, docutils, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.024x faster

# HPT report

- Reliability score: 78.43% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.08x