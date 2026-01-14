# Results vs. 3.13.0rc2

- fork: python
- ref: 1857a40807daeae3a1bf
- machine: darwin-arm64
- commit hash: 1857a40
- commit date: 2026-01-14
- overall geometric mean: 1.074x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.02x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.7 ms: 1.06x faster                                                    |
| sphinx         | 409 ms                                                         | 398 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.35x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 227 ms: 2.32x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 237 ms: 1.63x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 249 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.5 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.9 ms: 2.76x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                     |
| nbody          | 42.5 ms                                                        | 44.6 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.68 ms: 1.10x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.1 ms: 1.06x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.0 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.3 ms: 1.20x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.92 ms: 1.19x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 849 ms: 1.18x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 34.4 ms: 1.04x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 95.8 us: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.6 ms: 1.03x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 142 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.03 ms: 1.05x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.50 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.74 ms: 1.02x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.70 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.20x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.35x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 227 ms: 2.32x faster                                                     |
| mdp                              | 1.06 sec                                                       | 543 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 237 ms: 1.63x faster                                                     |
| k_core                           | 1.46 sec                                                       | 901 ms: 1.62x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.09 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 99.7 us: 1.45x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.44x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                     |
| go                               | 72.6 ms                                                        | 52.9 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.3 ms: 1.20x faster                                                    |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.19x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.92 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 249 ms: 1.18x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 849 ms: 1.18x faster                                                     |
| float                            | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.68 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.2 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 22.8 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.7 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.85 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.5 ms: 1.07x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.7 ms: 1.06x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 45.1 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 949 us: 1.05x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 624 ms: 1.04x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.4 ms: 1.04x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 310 ms: 1.04x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 95.8 us: 1.04x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 119 ms: 1.04x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.76 ms: 1.03x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 62.8 us: 1.03x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.6 ms: 1.03x faster                                                    |
| sphinx                           | 409 ms                                                         | 398 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.74 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.77 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 40.9 ns: 1.01x slower                                                    |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                     |
| 2to3                             | 112 ms                                                         | 113 ms: 1.02x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.0 ms: 1.02x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 973 ns: 1.03x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.10 ms: 1.03x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.3 ms: 1.03x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.1 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.2 ms: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.03 ms: 1.05x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.13 us: 1.05x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.8 ms: 1.05x slower                                                    |
| nbody                            | 42.5 ms                                                        | 44.6 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                     |
| raytrace                         | 109 ms                                                         | 115 ms: 1.05x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.7 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.70 ms: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.8 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 142 us: 1.09x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.50 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 36.7 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.5 ms: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.8 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 255 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.9 ms: 2.76x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (5): pycparser, logging_format, sympy_integrate, spectral_norm, thrift
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260114-3.15.0a4+-1857a40/bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.074x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.17x