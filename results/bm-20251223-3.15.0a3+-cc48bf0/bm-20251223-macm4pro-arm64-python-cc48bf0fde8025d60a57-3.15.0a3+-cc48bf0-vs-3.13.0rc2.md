# Results vs. 3.13.0rc2

- fork: python
- ref: cc48bf0fde8025d60a57
- machine: darwin-arm64
- commit hash: cc48bf0
- commit date: 2025-12-23
- overall geometric mean: 1.060x faster
- HPT reliability: 99.57%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| sphinx         | 409 ms                                                         | 402 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 223 ms: 2.35x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.34x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 235 ms: 1.64x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.92 ms: 1.08x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 123 ms: 1.19x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.2 ms: 2.84x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                     |
| nbody          | 42.5 ms                                                        | 47.5 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.75 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.8 ms: 1.02x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.1 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.92 ms: 1.19x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.7 ms: 1.03x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 97.2 us: 1.02x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.9 ms: 1.01x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.07 ms: 1.05x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.51 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                    |
| mako            | 4.41 ms                                                        | 4.78 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 223 ms: 2.35x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.34x faster                                                     |
| mdp                              | 1.06 sec                                                       | 550 ms: 1.92x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 235 ms: 1.64x faster                                                     |
| k_core                           | 1.46 sec                                                       | 916 ms: 1.60x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.10 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 104 us: 1.40x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.0 us: 1.38x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| go                               | 72.6 ms                                                        | 53.9 ms: 1.35x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.1 ms: 1.30x faster                                                    |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.92 ms: 1.19x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.10 us: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.17x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| float                            | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.75 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.92 ms: 1.08x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.5 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.1 ms: 1.07x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.90 ms: 1.06x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 952 us: 1.04x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                                    |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.2 ms: 1.03x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.7 ms: 1.03x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 97.2 us: 1.02x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.8 ms: 1.02x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 121 ms: 1.02x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 402 ms: 1.02x faster                                                     |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 61.9 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 320 ms: 1.01x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 647 ms: 1.00x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| pycparser                        | 470 ms                                                         | 475 ms: 1.01x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 44.2 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.80 ms: 1.01x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                    |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.29 us: 1.02x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 971 ns: 1.02x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.0 ms: 1.03x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.1 ms: 1.03x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.51 us: 1.03x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.0 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.13 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.05x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.07 ms: 1.05x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 45.0 ms: 1.05x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 51.0 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.0 ms: 1.07x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 171 ms: 1.07x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.32 us: 1.08x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.1 ms: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.78 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.51 ms: 1.09x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.1 ms: 1.10x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                     |
| nbody                            | 42.5 ms                                                        | 47.5 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.7 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 123 ms: 1.19x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 45.4 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 259 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.2 ms: 2.84x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (7): tomli_loads, genshi_text, typing_runtime_protocols, thrift, sympy_integrate, json, logging_silent
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251223-3.15.0a3+-cc48bf0/bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.060x faster

# HPT report

- Reliability score: 99.57% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.16x