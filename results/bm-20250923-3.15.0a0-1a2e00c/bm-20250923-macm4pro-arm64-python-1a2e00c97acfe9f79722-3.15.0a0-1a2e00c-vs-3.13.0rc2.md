# Results vs. 3.13.0rc2

- fork: python
- ref: 1a2e00c97acfe9f79722
- machine: darwin-arm64
- commit hash: 1a2e00c
- commit date: 2025-09-23
- overall geometric mean: 1.039x faster
- HPT reliability: 99.78%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                   |
| sphinx         | 409 ms                                                         | 398 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.94 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.3 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.1 ms: 2.98x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.8 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| nbody          | 42.5 ms                                                        | 46.5 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.71 ms: 1.10x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 47.4 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 889 ms: 1.12x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.3 ms: 1.06x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 97.2 us: 1.02x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.67 ms: 1.03x faster                                                   |
| mako            | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                   |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                    |
| mdp                              | 1.06 sec                                                       | 527 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                    |
| k_core                           | 1.46 sec                                                       | 948 ms: 1.54x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.0 us: 1.38x faster                                                   |
| deepcopy                         | 145 us                                                         | 106 us: 1.37x faster                                                    |
| go                               | 72.6 ms                                                        | 54.6 ms: 1.33x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.5 ms: 1.29x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.11 us: 1.17x faster                                                   |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.6 ms: 1.13x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 889 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.71 ms: 1.10x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.80 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 914 us: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.94 ms: 1.08x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.3 ms: 1.06x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.8 ms: 1.06x faster                                                   |
| float                            | 31.4 ms                                                        | 29.8 ms: 1.06x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.4 ms: 1.05x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 61.7 us: 1.05x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.3 ms: 1.05x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.74 ms: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 201 ms: 1.04x faster                                                    |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.28 ms: 1.03x faster                                                   |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.67 ms: 1.03x faster                                                   |
| fannkuch                         | 179 ms                                                         | 173 ms: 1.03x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                   |
| sphinx                           | 409 ms                                                         | 398 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 97.2 us: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 931 ns: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.4 ms: 1.02x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 43.0 ms: 1.02x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                  |
| regex_compile                    | 47.9 ms                                                        | 47.4 ms: 1.01x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.03 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.24 us: 1.00x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 324 ms: 1.01x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.47 us: 1.01x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                   |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 37.9 ms: 1.02x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.03x slower                                                   |
| pycparser                        | 470 ms                                                         | 484 ms: 1.03x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.6 ms: 1.03x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 427 us: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                    |
| pylint                           | 106 ms                                                         | 110 ms: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 54.9 ms: 1.05x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.5 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                   |
| raytrace                         | 109 ms                                                         | 116 ms: 1.07x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.33 us: 1.08x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.09x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                   |
| nbody                            | 42.5 ms                                                        | 46.5 ms: 1.09x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.2 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 36.9 ms: 1.10x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 47.1 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 41.7 ms: 1.10x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.97 ms: 1.11x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.20x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| many_optionals                   | 200 us                                                         | 321 us: 1.60x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.7 ms: 2.82x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.1 ms: 2.98x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (6): logging_silent, genshi_xml, pprint_pformat, thrift, regex_dna, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250923-3.15.0a0-1a2e00c/bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 99.78% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x