# Results vs. 3.13.0rc2

- fork: python
- ref: 4ddf505d9982dc8afead
- machine: darwin-arm64
- commit hash: 4ddf505
- commit date: 2025-06-20
- overall geometric mean: 1.023x faster
- HPT reliability: 77.55%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| html5lib       | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 252 ms: 1.61x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.50x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 269 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 271 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.97 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.6 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 254 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.3 ms: 3.09x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 50.2 ms: 1.18x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 919 ms: 1.09x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.46 ms: 1.04x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.3 ms: 1.04x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.5 us: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.7 ms: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 6.18 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.5 ms: 1.01x slower                                                   |
| mako            | 4.41 ms                                                        | 4.87 ms: 1.10x slower                                                   |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                    |
| mdp                              | 1.06 sec                                                       | 513 ms: 2.06x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 252 ms: 1.61x faster                                                    |
| k_core                           | 1.46 sec                                                       | 944 ms: 1.55x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.50x faster                                                    |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                   |
| go                               | 72.6 ms                                                        | 56.7 ms: 1.28x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 50.5 ms: 1.27x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.23x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 269 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 919 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 271 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 9.97 ms: 1.08x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 939 us: 1.06x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 61.8 us: 1.05x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.46 ms: 1.04x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.3 ms: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 201 ms: 1.03x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.76 ms: 1.03x faster                                                   |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| thrift                           | 309 us                                                         | 303 us: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.42 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.01x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.6 ms: 1.01x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.5 ms: 1.01x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.5 us: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.5 ms: 1.01x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 24.8 ms: 1.01x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                   |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 960 ns: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 63.7 ms: 1.02x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.1 ms: 1.02x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.10 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.83 ms: 1.03x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                   |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.18 ms: 1.04x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.5 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.05x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.53 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.0 ms: 1.06x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 500 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.8 ms: 1.07x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.31 us: 1.07x slower                                                   |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.4 ms: 1.09x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 134 ms: 1.09x slower                                                    |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 352 ms: 1.09x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 714 ms: 1.10x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.3 ms: 1.10x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.87 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.8 ms: 1.12x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.76 us: 1.13x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.13x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 48.8 ms: 1.14x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.56 us: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.6 ms: 1.18x slower                                                   |
| nbody                            | 42.5 ms                                                        | 50.2 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 254 ms: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.80 ms: 1.57x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.3 ms: 3.09x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 196 ns: 4.82x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (9): float, richards, genshi_text, python_startup, sphinx, pathlib, spectral_norm, docutils, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.023x faster

# HPT report

- Reliability score: 77.55% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x