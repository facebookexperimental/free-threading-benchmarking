# Results vs. 3.13.0rc2

- fork: python
- ref: ef06508f8ef1d2943b2f
- machine: darwin-arm64
- commit hash: ef06508
- commit date: 2025-03-23
- overall geometric mean: 1.014x slower
- HPT reliability: 94.90%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.08 sec: 1.03x slower                                                   |
| sphinx         | 409 ms                                                         | 422 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 266 ms: 1.98x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 267 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 267 ms: 1.52x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 267 ms: 1.45x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 153 ms: 1.22x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.20x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 155 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 270 ms: 1.12x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                     |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 43.7 ms: 1.01x slower                                                    |
| asyncio_websockets               | 194 ms                                                         | 196 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 136 ms: 1.32x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.8 ms: 3.17x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.09x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                     |
| float          | 31.4 ms                                                        | 33.0 ms: 1.05x slower                                                    |
| nbody          | 42.5 ms                                                        | 51.6 ms: 1.21x slower                                                    |
| Geometric mean | (ref)                                                          | 1.09x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.57 ms: 1.03x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 875 ms: 1.14x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.2 ms: 1.02x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 105 us: 1.05x slower                                                     |
| xml_etree_process    | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.07x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.14 ms: 1.11x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.95 ms: 1.04x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.60 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.9 ms: 1.02x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.7 ms: 1.07x slower                                                    |
| mako            | 4.41 ms                                                        | 4.82 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 16.0 ms: 1.28x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 266 ms: 1.98x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 267 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 267 ms: 1.52x faster                                                     |
| k_core                           | 1.46 sec                                                       | 975 ms: 1.50x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 267 ms: 1.45x faster                                                     |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.0 us: 1.27x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| go                               | 72.6 ms                                                        | 59.4 ms: 1.22x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 153 ms: 1.22x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.20x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 155 ms: 1.19x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.1 ms: 1.16x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 875 ms: 1.14x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 270 ms: 1.12x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                     |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| pyflate                          | 222 ms                                                         | 209 ms: 1.06x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 937 us: 1.06x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.57 ms: 1.03x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.2 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.11 sec: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 24.9 ms: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 957 ns: 1.01x slower                                                     |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 43.7 ms: 1.01x slower                                                    |
| asyncio_websockets               | 194 ms                                                         | 196 ms: 1.01x slower                                                     |
| thrift                           | 309 us                                                         | 313 us: 1.01x slower                                                     |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                     |
| telco                            | 3.07 ms                                                        | 3.14 ms: 1.02x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.9 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 45.7 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 332 ms: 1.03x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 670 ms: 1.03x slower                                                     |
| docutils                         | 1.05 sec                                                       | 1.08 sec: 1.03x slower                                                   |
| sphinx                           | 409 ms                                                         | 422 ms: 1.03x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 39.2 ms: 1.04x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.95 ms: 1.04x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 67.3 us: 1.04x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.5 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                     |
| pathlib                          | 11.1 ms                                                        | 11.6 ms: 1.05x slower                                                    |
| float                            | 31.4 ms                                                        | 33.0 ms: 1.05x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 105 us: 1.05x slower                                                     |
| mdp                              | 1.06 sec                                                       | 1.12 sec: 1.06x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 50.7 ms: 1.06x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.02 ms: 1.06x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.17 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.99 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.89 ms: 1.06x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.33 ms: 1.07x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.07x slower                                                    |
| pycparser                        | 470 ms                                                         | 503 ms: 1.07x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 10.7 ms: 1.07x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.1 ms: 1.07x slower                                                    |
| fannkuch                         | 179 ms                                                         | 192 ms: 1.08x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 103 ms: 1.08x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 172 ms: 1.08x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.64 us: 1.08x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.42 us: 1.08x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.9 ms: 1.09x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 135 ms: 1.09x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.82 ms: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.7 ns: 1.10x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.60 ms: 1.10x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.14 ms: 1.11x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.60 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.12x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.13x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 49.8 ms: 1.14x slower                                                    |
| raytrace                         | 109 ms                                                         | 125 ms: 1.15x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 49.3 ms: 1.15x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.87 us: 1.16x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.2 ms: 1.16x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.9 ms: 1.18x slower                                                    |
| many_optionals                   | 200 us                                                         | 240 us: 1.20x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                     |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 40.8 ms: 1.21x slower                                                    |
| nbody                            | 42.5 ms                                                        | 51.6 ms: 1.21x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.0 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 136 ms: 1.32x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.90 ms: 1.42x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.8 ms: 3.17x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (4): html5lib, async_tree_eager_cpu_io_mixed, regex_dna, richards
Ignored benchmarks (8) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250323-3.14.0a6+-ef06508/bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.014x slower

# HPT report

- Reliability score: 94.90% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.07x