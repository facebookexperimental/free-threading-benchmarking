# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: dc62b62
- commit date: 2025-11-24
- overall geometric mean: 1.073x faster
- HPT reliability: 96.35%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.05x slower                                     |
| html5lib       | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                    |
| sphinx         | 409 ms                                                         | 8.74 ms: 46.77x faster                                   |
| Geometric mean | (ref)                                                          | 3.53x faster                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 225 ms: 2.32x faster                                     |
| async_tree_eager_io              | 525 ms                                                         | 228 ms: 2.31x faster                                     |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                     |
| async_tree_io                    | 386 ms                                                         | 233 ms: 1.66x faster                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                     |
| async_tree_none_tg               | 133 ms                                                         | 97.9 ms: 1.35x faster                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.34x faster                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.16x faster                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                    |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                     |
| async_tree_eager                 | 43.2 ms                                                        | 42.9 ms: 1.01x faster                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.0 ms: 2.87x slower                                    |
| Geometric mean                   | (ref)                                                          | 1.18x faster                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                    |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                     |
| nbody          | 42.5 ms                                                        | 54.1 ms: 1.27x slower                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                    |
| regex_v8       | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                    |
| regex_compile  | 47.9 ms                                                        | 45.5 ms: 1.05x faster                                    |
| regex_dna      | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|----------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 818 ms: 1.22x faster                                     |
| json_dumps           | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.3 ms: 1.20x faster                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.6 ms: 1.07x faster                                    |
| unpickle_pure_python | 99.5 us                                                        | 93.9 us: 1.06x faster                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.5 ms: 1.02x faster                                    |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                    |
| pickle_pure_python   | 130 us                                                         | 132 us: 1.01x slower                                     |
| Geometric mean       | (ref)                                                          | 1.09x faster                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.10 ms: 1.05x slower                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.53 ms: 1.10x slower                                    |
| Geometric mean         | (ref)                                                          | 1.08x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|-----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.37 ms: 1.01x faster                                    |
| genshi_text     | 9.97 ms                                                        | 10.3 ms: 1.03x slower                                    |
| genshi_xml      | 21.4 ms                                                        | 23.6 ms: 1.10x slower                                    |
| django_template | 12.5 ms                                                        | 14.8 ms: 1.19x slower                                    |
| Geometric mean  | (ref)                                                          | 1.08x slower                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| sphinx                           | 409 ms                                                         | 8.74 ms: 46.77x faster                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 225 ms: 2.32x faster                                     |
| async_tree_eager_io              | 525 ms                                                         | 228 ms: 2.31x faster                                     |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                     |
| mdp                              | 1.06 sec                                                       | 622 ms: 1.70x faster                                     |
| async_tree_io                    | 386 ms                                                         | 233 ms: 1.66x faster                                     |
| richards                         | 22.1 ms                                                        | 14.6 ms: 1.51x faster                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.0 us: 1.50x faster                                    |
| richards_super                   | 24.7 ms                                                        | 16.6 ms: 1.49x faster                                    |
| deepcopy                         | 145 us                                                         | 102 us: 1.42x faster                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                     |
| async_tree_none_tg               | 133 ms                                                         | 97.9 ms: 1.35x faster                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.34x faster                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.7 ms: 1.26x faster                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.04 us: 1.25x faster                                    |
| tomli_loads                      | 1000 ms                                                        | 818 ms: 1.22x faster                                     |
| go                               | 72.6 ms                                                        | 59.5 ms: 1.22x faster                                    |
| json_dumps                       | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.3 ms: 1.20x faster                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                     |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.16x faster                                     |
| telco                            | 3.07 ms                                                        | 2.72 ms: 1.13x faster                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                    |
| pprint_safe_repr                 | 322 ms                                                         | 289 ms: 1.11x faster                                     |
| regex_v8                         | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                    |
| pprint_pformat                   | 650 ms                                                         | 591 ms: 1.10x faster                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.8 ms: 1.08x faster                                    |
| xml_etree_process                | 25.4 ms                                                        | 23.6 ms: 1.07x faster                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                    |
| unpickle_pure_python             | 99.5 us                                                        | 93.9 us: 1.06x faster                                    |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                    |
| regex_compile                    | 47.9 ms                                                        | 45.5 ms: 1.05x faster                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                    |
| create_gc_cycles                 | 993 us                                                         | 949 us: 1.05x faster                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.05 sec: 1.04x faster                                   |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.04x faster                                     |
| thrift                           | 309 us                                                         | 299 us: 1.03x faster                                     |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                     |
| fannkuch                         | 179 ms                                                         | 176 ms: 1.02x faster                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 61.5 ms: 1.02x faster                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                    |
| mako                             | 4.41 ms                                                        | 4.37 ms: 1.01x faster                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.9 ms: 1.01x faster                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                     |
| dulwich_log                      | 19.8 ms                                                        | 20.0 ms: 1.01x slower                                    |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                     |
| logging_simple                   | 2.24 us                                                        | 2.26 us: 1.01x slower                                    |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                    |
| html5lib                         | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                    |
| pickle_pure_python               | 130 us                                                         | 132 us: 1.01x slower                                     |
| logging_format                   | 2.45 us                                                        | 2.48 us: 1.01x slower                                    |
| pycparser                        | 470 ms                                                         | 479 ms: 1.02x slower                                     |
| sqlite_synth                     | 948 ns                                                         | 965 ns: 1.02x slower                                     |
| regex_dna                        | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                    |
| genshi_text                      | 9.97 ms                                                        | 10.3 ms: 1.03x slower                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.12 ms: 1.04x slower                                    |
| bench_thread_pool                | 412 us                                                         | 433 us: 1.05x slower                                     |
| 2to3                             | 112 ms                                                         | 118 ms: 1.05x slower                                     |
| python_startup                   | 8.63 ms                                                        | 9.10 ms: 1.05x slower                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.7 ms: 1.06x slower                                    |
| deltablue                        | 1.45 ms                                                        | 1.54 ms: 1.06x slower                                    |
| coverage                         | 31.2 ms                                                        | 33.7 ms: 1.08x slower                                    |
| comprehensions                   | 6.80 us                                                        | 7.41 us: 1.09x slower                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.53 ms: 1.10x slower                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.6 ms: 1.10x slower                                    |
| spectral_norm                    | 43.7 ms                                                        | 48.6 ms: 1.11x slower                                    |
| raytrace                         | 109 ms                                                         | 121 ms: 1.11x slower                                     |
| chaos                            | 24.3 ms                                                        | 27.4 ms: 1.13x slower                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.0 ms: 1.13x slower                                    |
| hexiom                           | 2.85 ms                                                        | 3.23 ms: 1.13x slower                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.02 ms: 1.14x slower                                    |
| nqueens                          | 37.2 ms                                                        | 42.7 ms: 1.15x slower                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.65 ms: 1.15x slower                                    |
| sympy_expand                     | 159 ms                                                         | 185 ms: 1.16x slower                                     |
| scimark_lu                       | 42.8 ms                                                        | 50.5 ms: 1.18x slower                                    |
| django_template                  | 12.5 ms                                                        | 14.8 ms: 1.19x slower                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                     |
| sympy_sum                        | 52.3 ms                                                        | 62.3 ms: 1.19x slower                                    |
| logging_silent                   | 40.6 ns                                                        | 48.6 ns: 1.20x slower                                    |
| sympy_str                        | 95.5 ms                                                        | 115 ms: 1.21x slower                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 45.9 ms: 1.21x slower                                    |
| pylint                           | 106 ms                                                         | 129 ms: 1.22x slower                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                     |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.23x slower                                    |
| nbody                            | 42.5 ms                                                        | 54.1 ms: 1.27x slower                                    |
| many_optionals                   | 200 us                                                         | 384 us: 1.91x slower                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.0 ms: 2.87x slower                                    |
| subparsers                       | 6.26 ms                                                        | 18.5 ms: 2.96x slower                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                             |

Benchmark hidden because not significant (1): typing_runtime_protocols
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, dask, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251124-3.15.0a2+-dc62b62-JIT/bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.073x faster

# HPT report

- Reliability score: 96.35% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.19x