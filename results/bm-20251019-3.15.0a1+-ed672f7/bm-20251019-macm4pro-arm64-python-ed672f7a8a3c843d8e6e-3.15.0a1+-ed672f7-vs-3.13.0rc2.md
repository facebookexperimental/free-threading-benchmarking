# Results vs. 3.13.0rc2

- fork: python
- ref: ed672f7a8a3c843d8e6e
- machine: darwin-arm64
- commit hash: ed672f7
- commit date: 2025-10-19
- overall geometric mean: 1.004x faster
- HPT reliability: 53.84%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.03x slower                                                     |
| html5lib       | 23.1 ms                                                        | 24.7 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.08x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 254 ms: 1.60x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.7 ms: 3.03x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 51.2 ms: 1.20x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.87 ms: 1.08x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.2 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.96 ms: 1.18x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.2 ms: 1.07x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 961 ms: 1.04x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 61.5 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.2 ms: 1.03x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 104 us: 1.05x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 150 us: 1.15x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.88 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                    |
| genshi_xml      | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| mako            | 4.41 ms                                                        | 5.01 ms: 1.14x slower                                                    |
| django_template | 12.5 ms                                                        | 15.9 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.08x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                     |
| mdp                              | 1.06 sec                                                       | 548 ms: 1.93x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 254 ms: 1.60x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                     |
| k_core                           | 1.46 sec                                                       | 991 ms: 1.48x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.33x faster                                                    |
| deepcopy                         | 145 us                                                         | 112 us: 1.29x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                     |
| go                               | 72.6 ms                                                        | 58.2 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 53.3 ms: 1.20x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.96 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.19 us: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.87 ms: 1.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 921 us: 1.08x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.2 ms: 1.07x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.88 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 961 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.5 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.5 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 207 ms: 1.00x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.49 ms: 1.00x faster                                                    |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.00x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 24.9 ms: 1.01x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 417 us: 1.01x slower                                                     |
| sqlite_synth                     | 948 ns                                                         | 965 ns: 1.02x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.6 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 66.0 us: 1.02x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 2.91 ms: 1.02x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.03x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.88 ms: 1.03x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.2 ms: 1.03x slower                                                    |
| thrift                           | 309 us                                                         | 321 us: 1.04x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 42.2 ns: 1.04x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 31.1 ms: 1.04x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 677 ms: 1.04x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 49.9 ms: 1.04x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.9 ms: 1.04x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 336 ms: 1.04x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 104 us: 1.05x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 50.2 ms: 1.05x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.88 ms: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 498 ms: 1.06x slower                                                     |
| fannkuch                         | 179 ms                                                         | 190 ms: 1.06x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                     |
| coverage                         | 31.2 ms                                                        | 33.3 ms: 1.07x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.55 ms: 1.07x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.7 ms: 1.07x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.63 us: 1.08x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 172 ms: 1.08x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.42 us: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 57.0 ms: 1.09x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.57 us: 1.11x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.11x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.2 ms: 1.12x slower                                                    |
| raytrace                         | 109 ms                                                         | 122 ms: 1.12x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 42.4 ms: 1.12x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.7 ms: 1.13x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.01 ms: 1.14x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 150 us: 1.15x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 49.7 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| nbody                            | 42.5 ms                                                        | 51.2 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.9 ms: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                     |
| many_optionals                   | 200 us                                                         | 375 us: 1.87x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 18.2 ms: 2.91x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.7 ms: 3.03x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (6): docutils, regex_dna, float, richards, json_loads, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251019-3.15.0a1+-ed672f7/bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1+-ed672f7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 53.84% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.15x