# Results vs. 3.13.0rc2

- fork: python
- ref: a936af924efc6e2fb59e
- machine: darwin-arm64
- commit hash: a936af9
- commit date: 2025-03-17
- overall geometric mean: 1.002x slower
- HPT reliability: 84.40%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                   |
| html5lib       | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                    |
| sphinx         | 409 ms                                                         | 414 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 257 ms: 2.04x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 260 ms: 2.00x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 260 ms: 1.56x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 266 ms: 1.45x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.21x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 153 ms: 1.21x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 155 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 136 ms: 1.32x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 90.4 ms: 3.13x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| float          | 31.4 ms                                                        | 32.5 ms: 1.03x slower                                                    |
| nbody          | 42.5 ms                                                        | 50.1 ms: 1.18x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 91.8 ms: 1.03x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 48.5 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 867 ms: 1.15x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.04x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 104 us: 1.04x slower                                                     |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 4.97 ms: 1.07x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.59 ms: 1.00x faster                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.38 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.5 ms: 1.05x slower                                                    |
| mako            | 4.41 ms                                                        | 4.78 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 257 ms: 2.04x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 260 ms: 2.00x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 260 ms: 1.56x faster                                                     |
| k_core                           | 1.46 sec                                                       | 963 ms: 1.52x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 266 ms: 1.45x faster                                                     |
| deepcopy                         | 145 us                                                         | 108 us: 1.35x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.30x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                     |
| go                               | 72.6 ms                                                        | 58.4 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.21x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 153 ms: 1.21x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 155 ms: 1.19x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.0 ms: 1.18x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 867 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 17.5 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.13x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 882 us: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| pyflate                          | 222 ms                                                         | 206 ms: 1.08x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.06 sec: 1.03x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 91.8 ms: 1.03x faster                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 36.8 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| connected_components             | 208 ms                                                         | 204 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                     |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| python_startup                   | 8.63 ms                                                        | 8.59 ms: 1.00x faster                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 44.6 ms: 1.01x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 414 ms: 1.01x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 48.5 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 662 ms: 1.02x slower                                                     |
| thrift                           | 309 us                                                         | 316 us: 1.02x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 49.1 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.0 ms: 1.03x slower                                                    |
| richards                         | 22.1 ms                                                        | 22.7 ms: 1.03x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.4 ms: 1.03x slower                                                    |
| mdp                              | 1.06 sec                                                       | 1.09 sec: 1.03x slower                                                   |
| float                            | 31.4 ms                                                        | 32.5 ms: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 2.96 ms: 1.04x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 67.2 us: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.04x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 104 us: 1.04x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 31.3 ms: 1.05x slower                                                    |
| pycparser                        | 470 ms                                                         | 492 ms: 1.05x slower                                                     |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.25 ms: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 433 us: 1.05x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 10.5 ms: 1.05x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.59 us: 1.06x slower                                                    |
| fannkuch                         | 179 ms                                                         | 189 ms: 1.06x slower                                                     |
| sqlglot_optimize                 | 22.2 ms                                                        | 23.5 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.27 ms: 1.07x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                     |
| json_dumps                       | 4.65 ms                                                        | 4.97 ms: 1.07x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.39 us: 1.07x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 171 ms: 1.07x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.1 ms: 1.07x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.38 ms: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.92 ms: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.13 ms: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.78 ms: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.0 ns: 1.08x slower                                                    |
| sqlglot_transpile                | 637 us                                                         | 691 us: 1.09x slower                                                     |
| sqlglot_normalize                | 116 ms                                                         | 126 ms: 1.09x slower                                                     |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.59 ms: 1.09x slower                                                    |
| sqlglot_parse                    | 519 us                                                         | 569 us: 1.10x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 48.6 ms: 1.11x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.12x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.71 us: 1.13x slower                                                    |
| raytrace                         | 109 ms                                                         | 124 ms: 1.14x slower                                                     |
| chaos                            | 24.3 ms                                                        | 27.8 ms: 1.15x slower                                                    |
| many_optionals                   | 200 us                                                         | 232 us: 1.16x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 43.2 ms: 1.16x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.3 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| nbody                            | 42.5 ms                                                        | 50.1 ms: 1.18x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 50.7 ms: 1.19x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 40.1 ms: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 136 ms: 1.32x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.59 ms: 1.37x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 90.4 ms: 3.13x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (5): async_tree_eager, 2to3, sqlite_synth, regex_v8, xml_etree_iterparse
Ignored benchmarks (4) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, tornado_http

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 84.40% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.07x