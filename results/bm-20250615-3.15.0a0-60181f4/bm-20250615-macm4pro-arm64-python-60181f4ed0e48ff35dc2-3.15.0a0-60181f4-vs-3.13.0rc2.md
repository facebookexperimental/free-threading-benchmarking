# Results vs. 3.13.0rc2

- fork: python
- ref: 60181f4ed0e48ff35dc2
- machine: darwin-arm64
- commit hash: 60181f4
- commit date: 2025-06-15
- overall geometric mean: 1.028x faster
- HPT reliability: 88.83%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.03x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| html5lib       | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 255 ms: 1.52x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 268 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.0 ms: 3.04x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.0 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 47.4 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.79 ms: 1.09x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 47.8 ms: 1.00x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 99.7 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 901 ms: 1.11x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.44 ms: 1.05x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 97.6 us: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.0 ms: 1.02x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (2): json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.86 ms: 1.01x faster                                                   |
| mako            | 4.41 ms                                                        | 4.81 ms: 1.09x slower                                                   |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                    |
| mdp                              | 1.06 sec                                                       | 513 ms: 2.06x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| k_core                           | 1.46 sec                                                       | 950 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 255 ms: 1.52x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.3 us: 1.34x faster                                                   |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                    |
| go                               | 72.6 ms                                                        | 55.6 ms: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.8 ms: 1.28x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                    |
| pyflate                          | 222 ms                                                         | 193 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 268 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.12x faster                                                   |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.11x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 901 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.79 ms: 1.09x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.08x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| float                            | 31.4 ms                                                        | 30.0 ms: 1.05x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.44 ms: 1.05x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 61.7 us: 1.05x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 949 us: 1.05x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.74 ms: 1.04x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                   |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.2 ms: 1.02x faster                                                   |
| connected_components             | 208 ms                                                         | 203 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                   |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 97.6 us: 1.02x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.6 ms: 1.02x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.3 ms: 1.02x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.0 ms: 1.02x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.02x faster                                                   |
| thrift                           | 309 us                                                         | 304 us: 1.02x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.86 ms: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.45 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 47.8 ms: 1.00x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| python_startup                   | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.2 ms: 1.01x slower                                                   |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 962 ns: 1.02x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.1 ms: 1.02x slower                                                   |
| 2to3                             | 112 ms                                                         | 114 ms: 1.03x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.84 ms: 1.04x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.0 ms: 1.04x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.12 ms: 1.04x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.04x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 45.5 ms: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 432 us: 1.05x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 99.7 ms: 1.05x slower                                                   |
| pycparser                        | 470 ms                                                         | 496 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.9 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.0 ms: 1.07x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.08x slower                                                   |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 349 ms: 1.08x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.39 us: 1.09x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 707 ms: 1.09x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.81 ms: 1.09x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.11x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.4 ms: 1.12x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.6 ms: 1.12x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.0 ms: 1.12x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.74 us: 1.12x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.55 us: 1.14x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.7 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                   |
| many_optionals                   | 200 us                                                         | 247 us: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.71 ms: 1.55x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.0 ms: 3.04x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 196 ns: 4.84x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (5): pathlib, sphinx, genshi_xml, json_loads, xml_etree_parse
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250615-3.15.0a0-60181f4/bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.028x faster

# HPT report

- Reliability score: 88.83% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x