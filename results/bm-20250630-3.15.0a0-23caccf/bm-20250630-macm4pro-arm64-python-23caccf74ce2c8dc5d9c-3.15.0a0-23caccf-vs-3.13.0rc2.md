# Results vs. 3.13.0rc2

- fork: python
- ref: 23caccf74ce2c8dc5d9c
- machine: darwin-arm64
- commit hash: 23caccf
- commit date: 2025-06-30
- overall geometric mean: 1.019x faster
- HPT reliability: 55.76%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.07 sec: 1.02x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.6 ms: 1.06x slower                                                   |
| sphinx         | 409 ms                                                         | 415 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 254 ms: 2.07x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 258 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 257 ms: 1.58x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 257 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 269 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 272 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.5 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 195 ms: 1.00x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 254 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 133 ms: 1.30x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.2 ms: 3.08x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                   |
| pidigits       | 166 ms                                                         | 174 ms: 1.05x slower                                                    |
| nbody          | 42.5 ms                                                        | 47.8 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 99.5 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 910 ms: 1.10x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.47 ms: 1.04x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.9 ms: 1.03x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 97.4 us: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.6 ms: 1.01x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (2): xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.00 ms: 1.04x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.41 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                   |
| mako            | 4.41 ms                                                        | 4.91 ms: 1.11x slower                                                   |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.25x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 254 ms: 2.07x faster                                                    |
| mdp                              | 1.06 sec                                                       | 514 ms: 2.06x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 258 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 257 ms: 1.58x faster                                                    |
| k_core                           | 1.46 sec                                                       | 963 ms: 1.52x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 257 ms: 1.50x faster                                                    |
| deepcopy                         | 145 us                                                         | 111 us: 1.30x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.29x faster                                                   |
| go                               | 72.6 ms                                                        | 56.9 ms: 1.27x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 51.0 ms: 1.26x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.22x faster                                                    |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 269 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.11x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 910 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 272 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| float                            | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 62.0 us: 1.04x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.47 ms: 1.04x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.0 ms: 1.03x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.9 ms: 1.03x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 97.4 us: 1.02x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.5 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.01x faster                                                   |
| connected_components             | 208 ms                                                         | 205 ms: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 306 us: 1.01x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.9 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.6 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 178 ms: 1.00x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 990 us: 1.00x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.55 ms: 1.00x slower                                                   |
| asyncio_websockets               | 194 ms                                                         | 195 ms: 1.00x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 24.8 ms: 1.01x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 37.5 ms: 1.01x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 957 ns: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                   |
| sphinx                           | 409 ms                                                         | 415 ms: 1.01x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 44.6 ms: 1.02x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.07 sec: 1.02x slower                                                  |
| pprint_pformat                   | 650 ms                                                         | 667 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 331 ms: 1.03x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.00 ms: 1.04x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.8 ms: 1.05x slower                                                   |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 432 us: 1.05x slower                                                    |
| pidigits                         | 166 ms                                                         | 174 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 99.5 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.87 ms: 1.05x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.53 ms: 1.06x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.0 ms: 1.06x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.16 ms: 1.06x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.6 ms: 1.06x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.39 us: 1.07x slower                                                   |
| pycparser                        | 470 ms                                                         | 503 ms: 1.07x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.41 ms: 1.08x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.9 ms: 1.09x slower                                                   |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.6 ms: 1.10x slower                                                   |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.51 us: 1.10x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.91 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.6 ms: 1.12x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.8 ms: 1.12x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.7 ms: 1.13x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 49.3 ms: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.2 ms: 1.19x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 254 ms: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.25x slower                                                   |
| many_optionals                   | 200 us                                                         | 255 us: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 133 ms: 1.30x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.87 ms: 1.58x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.2 ms: 3.08x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (5): xml_etree_parse, pathlib, genshi_text, json_loads, logging_silent
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250630-3.15.0a0-23caccf/bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.019x faster

# HPT report

- Reliability score: 55.76% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x