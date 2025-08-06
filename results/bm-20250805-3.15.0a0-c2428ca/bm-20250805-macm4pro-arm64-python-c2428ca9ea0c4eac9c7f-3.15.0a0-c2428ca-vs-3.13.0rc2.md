# Results vs. 3.13.0rc2

- fork: python
- ref: c2428ca9ea0c4eac9c7f
- machine: darwin-arm64
- commit hash: c2428ca
- commit date: 2025-08-05
- overall geometric mean: 1.018x faster
- HPT reliability: 79.92%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.13x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.0 ms: 3.04x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.5 ms: 1.03x faster                                                   |
| pidigits       | 166 ms                                                         | 166 ms: 1.00x faster                                                    |
| nbody          | 42.5 ms                                                        | 48.2 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.74 ms: 1.10x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.50 ms: 1.07x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 928 ms: 1.08x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.5 ms: 1.06x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.55 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 100 us: 1.01x slower                                                    |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                   |
| mako            | 4.41 ms                                                        | 4.85 ms: 1.10x slower                                                   |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.13x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| mdp                              | 1.06 sec                                                       | 539 ms: 1.96x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| k_core                           | 1.46 sec                                                       | 954 ms: 1.53x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                    |
| deepcopy                         | 145 us                                                         | 111 us: 1.30x faster                                                    |
| go                               | 72.6 ms                                                        | 55.9 ms: 1.30x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.29x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.4 ms: 1.25x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.12x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.74 ms: 1.10x faster                                                   |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 928 ms: 1.08x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.50 ms: 1.07x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.5 ms: 1.06x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 948 us: 1.05x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.1 ms: 1.04x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.8 ms: 1.04x faster                                                   |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.04x faster                                                    |
| connected_components             | 208 ms                                                         | 201 ms: 1.03x faster                                                    |
| float                            | 31.4 ms                                                        | 30.5 ms: 1.03x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.55 ms: 1.02x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.79 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 63.9 us: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 307 us: 1.01x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.05 ms: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.8 ms: 1.00x faster                                                   |
| pidigits                         | 166 ms                                                         | 166 ms: 1.00x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 952 ns: 1.00x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 100 us: 1.01x slower                                                    |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 326 ms: 1.01x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 658 ms: 1.01x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.09 ms: 1.02x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.6 ms: 1.04x slower                                                   |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.57 us: 1.05x slower                                                   |
| pycparser                        | 470 ms                                                         | 496 ms: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.36 us: 1.06x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.53 ms: 1.06x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 436 us: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.08x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.92 ms: 1.08x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.6 ms: 1.08x slower                                                   |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.85 ms: 1.10x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.55 us: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.11x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.0 ms: 1.12x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.7 ms: 1.13x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.2 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.3 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| many_optionals                   | 200 us                                                         | 323 us: 1.61x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.4 ms: 2.78x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.0 ms: 3.04x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (5): genshi_text, sympy_integrate, sphinx, logging_silent, spectral_norm
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.018x faster

# HPT report

- Reliability score: 79.92% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x