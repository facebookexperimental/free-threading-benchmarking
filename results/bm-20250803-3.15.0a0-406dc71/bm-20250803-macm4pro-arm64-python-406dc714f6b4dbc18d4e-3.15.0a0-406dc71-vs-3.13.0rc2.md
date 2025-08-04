# Results vs. 3.13.0rc2

- fork: python
- ref: 406dc714f6b4dbc18d4e
- machine: darwin-arm64
- commit hash: 406dc71
- commit date: 2025-08-03
- overall geometric mean: 1.024x faster
- HPT reliability: 95.26%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                  |
| html5lib       | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.29x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.97 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.1 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.9 ms: 3.00x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 31.0 ms: 1.01x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 48.5 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.58 ms: 1.12x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 96.7 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 927 ms: 1.08x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.1 ms: 1.07x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.49 ms: 1.04x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.9 ms: 1.03x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 99.0 us: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.2 ms: 1.00x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 6.19 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.86 ms: 1.01x faster                                                   |
| mako            | 4.41 ms                                                        | 4.90 ms: 1.11x slower                                                   |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                    |
| mdp                              | 1.06 sec                                                       | 538 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                    |
| k_core                           | 1.46 sec                                                       | 959 ms: 1.53x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.3 us: 1.34x faster                                                   |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                    |
| go                               | 72.6 ms                                                        | 55.9 ms: 1.30x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.29x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.8 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.14x faster                                                   |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.58 ms: 1.12x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 9.97 ms: 1.08x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 927 ms: 1.08x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.1 ms: 1.07x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 941 us: 1.06x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.1 ms: 1.05x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.2 ms: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.49 ms: 1.04x faster                                                   |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.04x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.9 ms: 1.03x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 60.9 ms: 1.03x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.79 ms: 1.02x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.5 us: 1.02x faster                                                   |
| float                            | 31.4 ms                                                        | 31.0 ms: 1.01x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.86 ms: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 40.3 ns: 1.01x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.04 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 99.0 us: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.00x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.49 ms: 1.00x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.8 ms: 1.00x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                  |
| pprint_safe_repr                 | 322 ms                                                         | 323 ms: 1.00x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 655 ms: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 957 ns: 1.01x slower                                                    |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                    |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 44.4 ms: 1.01x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 96.7 ms: 1.02x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.5 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.6 ms: 1.03x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.4 ms: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.19 ms: 1.04x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 492 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.05x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.59 us: 1.06x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 438 us: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.1 ms: 1.07x slower                                                   |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.93 ms: 1.08x slower                                                   |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.5 ms: 1.09x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.43 us: 1.09x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.1 ms: 1.10x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.4 ms: 1.11x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.90 ms: 1.11x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.5 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.3 ms: 1.14x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 50.1 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.21x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| many_optionals                   | 200 us                                                         | 315 us: 1.57x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.2 ms: 2.74x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.9 ms: 3.00x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (4): sphinx, thrift, genshi_xml, python_startup
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250803-3.15.0a0-406dc71/bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.024x faster

# HPT report

- Reliability score: 95.26% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x