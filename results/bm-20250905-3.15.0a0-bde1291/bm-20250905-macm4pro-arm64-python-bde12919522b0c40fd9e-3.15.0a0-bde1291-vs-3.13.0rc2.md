# Results vs. 3.13.0rc2

- fork: python
- ref: bde12919522b0c40fd9e
- machine: darwin-arm64
- commit hash: bde1291
- commit date: 2025-09-05
- overall geometric mean: 1.029x faster
- HPT reliability: 95.26%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.12x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 251 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 252 ms: 1.61x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.88 ms: 1.09x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.7 ms: 3.00x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.8 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 47.3 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.1 ms: 1.00x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.83 ms: 1.21x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 880 ms: 1.14x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 97.1 us: 1.02x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.2 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 65.6 ms: 1.05x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.68 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.22 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                   |
| mako            | 4.41 ms                                                        | 4.90 ms: 1.11x slower                                                   |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.12x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 251 ms: 2.08x faster                                                    |
| mdp                              | 1.06 sec                                                       | 534 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 252 ms: 1.61x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                    |
| k_core                           | 1.46 sec                                                       | 954 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 106 us: 1.37x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.1 us: 1.37x faster                                                   |
| go                               | 72.6 ms                                                        | 55.6 ms: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.7 ms: 1.29x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.83 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 880 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.13x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.73 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 9.88 ms: 1.09x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 920 us: 1.08x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| float                            | 31.4 ms                                                        | 29.8 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.3 ms: 1.03x faster                                                   |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 97.1 us: 1.02x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.2 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.2 ms: 1.02x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.79 ms: 1.02x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.4 ms: 1.02x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 63.5 us: 1.02x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.40 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 40.3 ns: 1.01x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 43.6 ms: 1.00x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.1 ms: 1.00x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.68 ms: 1.01x slower                                                   |
| thrift                           | 309 us                                                         | 311 us: 1.01x slower                                                    |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 325 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 960 ns: 1.01x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.27 us: 1.01x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.49 us: 1.02x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 661 ms: 1.02x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.3 ms: 1.03x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 425 us: 1.03x slower                                                    |
| pycparser                        | 470 ms                                                         | 490 ms: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.22 ms: 1.04x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 50.1 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 65.6 ms: 1.05x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.06x slower                                                    |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.9 ms: 1.07x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.91 ms: 1.08x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.36 us: 1.08x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.3 ms: 1.08x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.09x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 36.9 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 41.8 ms: 1.11x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.90 ms: 1.11x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.3 ms: 1.11x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.6 ms: 1.12x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.1 ms: 1.12x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| many_optionals                   | 200 us                                                         | 315 us: 1.57x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.1 ms: 2.73x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.7 ms: 3.00x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (3): genshi_text, sphinx, gc_traversal
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250905-3.15.0a0-bde1291/bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.029x faster

# HPT report

- Reliability score: 95.26% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x