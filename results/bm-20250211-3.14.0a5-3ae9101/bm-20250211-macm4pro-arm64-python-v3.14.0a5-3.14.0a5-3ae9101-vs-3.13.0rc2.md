# Results vs. 3.13.0rc2

- fork: python
- ref: v3.14.0a5
- machine: darwin-arm64
- commit hash: 3ae9101
- commit date: 2025-02-11
- overall geometric mean: 1.014x faster
- HPT reliability: 78.06%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.01x faster                                         |
| html5lib       | 23.1 ms                                                        | 22.1 ms: 1.05x faster                                        |
| Geometric mean | (ref)                                                          | 1.02x faster                                                 |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 255 ms: 2.06x faster                                         |
| async_tree_eager_io_tg           | 521 ms                                                         | 267 ms: 1.95x faster                                         |
| async_tree_io_tg                 | 405 ms                                                         | 262 ms: 1.54x faster                                         |
| async_tree_io                    | 386 ms                                                         | 262 ms: 1.47x faster                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 153 ms: 1.22x faster                                         |
| async_tree_none                  | 142 ms                                                         | 118 ms: 1.21x faster                                         |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.20x faster                                         |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.20x faster                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                         |
| async_generators                 | 193 ms                                                         | 175 ms: 1.11x faster                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.11x faster                                         |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                         |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                         |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.01x faster                                         |
| async_tree_eager                 | 43.2 ms                                                        | 44.0 ms: 1.02x slower                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 139 ms: 1.35x slower                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.7 ms: 3.20x slower                                        |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                         |
| nbody          | 42.5 ms                                                        | 50.0 ms: 1.18x slower                                        |
| Geometric mean | (ref)                                                          | 1.05x slower                                                 |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                        |
| regex_dna      | 94.6 ms                                                        | 93.6 ms: 1.01x faster                                        |
| regex_compile  | 47.9 ms                                                        | 47.4 ms: 1.01x faster                                        |
| regex_v8       | 10.7 ms                                                        | 10.8 ms: 1.01x slower                                        |
| Geometric mean | (ref)                                                          | 1.03x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 826 ms: 1.21x faster                                         |
| xml_etree_parse      | 62.4 ms                                                        | 62.1 ms: 1.00x faster                                        |
| unpickle_pure_python | 99.5 us                                                        | 99.7 us: 1.00x slower                                        |
| xml_etree_generate   | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                        |
| xml_etree_process    | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                        |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                        |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                         |
| json_dumps           | 4.65 ms                                                        | 5.02 ms: 1.08x slower                                        |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                 |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.60 ms: 1.00x faster                                        |
| python_startup_no_site | 5.95 ms                                                        | 5.98 ms: 1.00x slower                                        |
| Geometric mean         | (ref)                                                          | 1.00x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 20.7 ms: 1.03x faster                                        |
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                        |
| mako            | 4.41 ms                                                        | 4.73 ms: 1.07x slower                                        |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                        |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 255 ms: 2.06x faster                                         |
| async_tree_eager_io_tg           | 521 ms                                                         | 267 ms: 1.95x faster                                         |
| k_core                           | 1.46 sec                                                       | 943 ms: 1.55x faster                                         |
| async_tree_io_tg                 | 405 ms                                                         | 262 ms: 1.54x faster                                         |
| async_tree_io                    | 386 ms                                                         | 262 ms: 1.47x faster                                         |
| deepcopy                         | 145 us                                                         | 104 us: 1.40x faster                                         |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                        |
| go                               | 72.6 ms                                                        | 56.9 ms: 1.27x faster                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 153 ms: 1.22x faster                                         |
| async_tree_none                  | 142 ms                                                         | 118 ms: 1.21x faster                                         |
| tomli_loads                      | 1000 ms                                                        | 826 ms: 1.21x faster                                         |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.20x faster                                         |
| scimark_sor                      | 64.0 ms                                                        | 53.4 ms: 1.20x faster                                        |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.20x faster                                         |
| deepcopy_reduce                  | 1.30 us                                                        | 1.11 us: 1.17x faster                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                         |
| pyflate                          | 222 ms                                                         | 199 ms: 1.12x faster                                         |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                        |
| async_generators                 | 193 ms                                                         | 175 ms: 1.11x faster                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.11x faster                                         |
| create_gc_cycles                 | 993 us                                                         | 903 us: 1.10x faster                                         |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                         |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                        |
| html5lib                         | 23.1 ms                                                        | 22.1 ms: 1.05x faster                                        |
| connected_components             | 208 ms                                                         | 199 ms: 1.04x faster                                         |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                         |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                         |
| bench_mp_pool                    | 37.8 ms                                                        | 36.6 ms: 1.03x faster                                        |
| genshi_xml                       | 21.4 ms                                                        | 20.7 ms: 1.03x faster                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.74 ms: 1.02x faster                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                         |
| richards                         | 22.1 ms                                                        | 21.7 ms: 1.01x faster                                        |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                         |
| 2to3                             | 112 ms                                                         | 110 ms: 1.01x faster                                         |
| richards_super                   | 24.7 ms                                                        | 24.4 ms: 1.01x faster                                        |
| regex_dna                        | 94.6 ms                                                        | 93.6 ms: 1.01x faster                                        |
| regex_compile                    | 47.9 ms                                                        | 47.4 ms: 1.01x faster                                        |
| pprint_pformat                   | 650 ms                                                         | 644 ms: 1.01x faster                                         |
| pprint_safe_repr                 | 322 ms                                                         | 320 ms: 1.01x faster                                         |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                         |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.01x faster                                         |
| xml_etree_parse                  | 62.4 ms                                                        | 62.1 ms: 1.00x faster                                        |
| python_startup                   | 8.63 ms                                                        | 8.60 ms: 1.00x faster                                        |
| sqlalchemy_declarative           | 44.4 ms                                                        | 44.3 ms: 1.00x faster                                        |
| unpickle_pure_python             | 99.5 us                                                        | 99.7 us: 1.00x slower                                        |
| python_startup_no_site           | 5.95 ms                                                        | 5.98 ms: 1.00x slower                                        |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                        |
| scimark_fft                      | 124 ms                                                         | 124 ms: 1.01x slower                                         |
| regex_v8                         | 10.7 ms                                                        | 10.8 ms: 1.01x slower                                        |
| thrift                           | 309 us                                                         | 312 us: 1.01x slower                                         |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                        |
| mdp                              | 1.06 sec                                                       | 1.08 sec: 1.02x slower                                       |
| async_tree_eager                 | 43.2 ms                                                        | 44.0 ms: 1.02x slower                                        |
| xml_etree_generate               | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                        |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.11 ms: 1.02x slower                                        |
| hexiom                           | 2.85 ms                                                        | 2.91 ms: 1.02x slower                                        |
| pycparser                        | 470 ms                                                         | 481 ms: 1.02x slower                                         |
| spectral_norm                    | 43.7 ms                                                        | 44.8 ms: 1.02x slower                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.6 ms: 1.02x slower                                        |
| sqlglot_transpile                | 637 us                                                         | 653 us: 1.03x slower                                         |
| sqlglot_parse                    | 519 us                                                         | 533 us: 1.03x slower                                         |
| gc_traversal                     | 2.04 ms                                                        | 2.10 ms: 1.03x slower                                        |
| telco                            | 3.07 ms                                                        | 3.17 ms: 1.03x slower                                        |
| sqlglot_optimize                 | 22.2 ms                                                        | 23.1 ms: 1.04x slower                                        |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                         |
| xml_etree_process                | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                        |
| logging_simple                   | 2.24 us                                                        | 2.33 us: 1.04x slower                                        |
| sympy_sum                        | 52.3 ms                                                        | 54.6 ms: 1.04x slower                                        |
| sympy_str                        | 95.5 ms                                                        | 99.8 ms: 1.04x slower                                        |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                        |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                        |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                         |
| sympy_integrate                  | 7.53 ms                                                        | 7.96 ms: 1.06x slower                                        |
| logging_format                   | 2.45 us                                                        | 2.59 us: 1.06x slower                                        |
| logging_silent                   | 40.6 ns                                                        | 43.4 ns: 1.07x slower                                        |
| deltablue                        | 1.45 ms                                                        | 1.55 ms: 1.07x slower                                        |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                         |
| mako                             | 4.41 ms                                                        | 4.73 ms: 1.07x slower                                        |
| sqlglot_normalize                | 116 ms                                                         | 124 ms: 1.07x slower                                         |
| json_dumps                       | 4.65 ms                                                        | 5.02 ms: 1.08x slower                                        |
| pylint                           | 106 ms                                                         | 115 ms: 1.08x slower                                         |
| crypto_pyaes                     | 33.6 ms                                                        | 36.6 ms: 1.09x slower                                        |
| nqueens                          | 37.2 ms                                                        | 40.6 ms: 1.09x slower                                        |
| comprehensions                   | 6.80 us                                                        | 7.44 us: 1.09x slower                                        |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.11x slower                                        |
| chaos                            | 24.3 ms                                                        | 27.3 ms: 1.13x slower                                        |
| scimark_lu                       | 42.8 ms                                                        | 48.3 ms: 1.13x slower                                        |
| raytrace                         | 109 ms                                                         | 124 ms: 1.14x slower                                         |
| many_optionals                   | 200 us                                                         | 229 us: 1.14x slower                                         |
| nbody                            | 42.5 ms                                                        | 50.0 ms: 1.18x slower                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                         |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                        |
| subparsers                       | 6.26 ms                                                        | 8.42 ms: 1.34x slower                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 139 ms: 1.35x slower                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.7 ms: 3.20x slower                                        |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                 |

Benchmark hidden because not significant (9): docutils, xml_etree_iterparse, sphinx, meteor_contest, dulwich_log, float, typing_runtime_protocols, json, sqlite_synth
Ignored benchmarks (4) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, tornado_http

- Geometric mean (including insignificant results): 1.014x faster

# HPT report

- Reliability score: 78.06% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.07x