# Results vs. 3.12.6

- fork: python
- ref: cc48bf0fde8025d60a57
- machine: darwin-arm64
- commit hash: cc48bf0
- commit date: 2025-12-23
- overall geometric mean: 1.144x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 114 ms: 1.00x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| sphinx         | 434 ms                                                   | 402 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.22x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 235 ms: 1.95x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.71x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.92 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.6 ms: 1.10x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 123 ms: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.2 ms: 2.56x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.31x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| nbody          | 54.2 ms                                                  | 47.5 ms: 1.14x faster                                                    |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                    | 1.14x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.8 ms: 1.17x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.1 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.75 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.0 ms: 1.29x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.7 ms: 1.12x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.9 ms: 1.10x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.2 us: 1.06x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.03x slower                                                     |
| tomli_loads          | 957 ms                                                   | 995 ms: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.07 ms: 1.13x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.51 ms: 1.14x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.94 ms: 1.05x faster                                                    |
| django_template | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (2): genshi_xml, mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.10 ms: 5.06x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.22x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                     |
| mdp                              | 1.09 sec                                                 | 550 ms: 1.99x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 235 ms: 1.95x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.71x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| deepcopy                         | 161 us                                                   | 104 us: 1.56x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.0 us: 1.53x faster                                                    |
| float                            | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.92 ms: 1.37x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.32 us: 1.35x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.10 us: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| go                               | 70.0 ms                                                  | 53.9 ms: 1.30x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.0 ms: 1.29x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.9 ns: 1.24x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.1 ms: 1.24x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.2 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| k_core                           | 1.12 sec                                                 | 916 ms: 1.22x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.7 ms: 1.17x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 121 ms: 1.17x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.48 ms: 1.17x faster                                                    |
| pyflate                          | 216 ms                                                   | 185 ms: 1.17x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 46.8 ms: 1.17x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.6 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| chaos                            | 28.9 ms                                                  | 25.0 ms: 1.16x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.80 ms: 1.15x faster                                                    |
| nbody                            | 54.2 ms                                                  | 47.5 ms: 1.14x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 45.0 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.29 us: 1.12x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.7 ms: 1.12x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.51 us: 1.11x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.2 ms: 1.10x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.5 us: 1.10x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.9 ms: 1.10x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.1 ms: 1.10x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.77 ms: 1.10x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.6 ms: 1.10x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.5 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.1 ms: 1.08x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 402 ms: 1.08x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.54 ms: 1.06x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 97.2 us: 1.06x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.94 ms: 1.05x faster                                                    |
| pycparser                        | 497 ms                                                   | 475 ms: 1.05x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| thrift                           | 322 us                                                   | 309 us: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                     |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 56.0 ms: 1.03x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 647 ms: 1.03x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 320 ms: 1.03x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 97.1 ms: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| 2to3                             | 114 ms                                                   | 114 ms: 1.00x faster                                                     |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.75 ms: 1.02x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 171 ms: 1.03x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.03x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                     |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                     |
| tomli_loads                      | 957 ms                                                   | 995 ms: 1.04x slower                                                     |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.13 ms: 1.06x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 51.0 ms: 1.07x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 123 ms: 1.09x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.90 ms: 1.11x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.07 ms: 1.13x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.51 ms: 1.14x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.4 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.15x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 952 us: 1.15x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.0 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 259 us: 1.33x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.2 ms: 2.56x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                             |

Benchmark hidden because not significant (4): genshi_xml, mako, sqlite_synth, json_loads
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251223-3.15.0a3+-cc48bf0/bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.144x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.20x