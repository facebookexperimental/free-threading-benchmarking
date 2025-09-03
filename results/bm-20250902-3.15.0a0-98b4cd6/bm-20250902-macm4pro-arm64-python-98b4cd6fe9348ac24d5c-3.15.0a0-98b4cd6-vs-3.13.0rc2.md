# Results vs. 3.13.0rc2

- fork: python
- ref: 98b4cd6fe9348ac24d5c
- machine: darwin-arm64
- commit hash: 98b4cd6
- commit date: 2025-09-02
- overall geometric mean: 1.017x faster
- HPT reliability: 77.33%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.02x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.4 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 250 ms: 2.09x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.97 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.8 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.8 ms: 3.00x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 47.6 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 97.5 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 916 ms: 1.09x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.9 ms: 1.05x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.5 us: 1.01x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 62.8 ms: 1.01x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.03x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.83 ms: 1.02x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.31 ms: 1.06x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.9 ms: 1.02x slower                                                   |
| mako            | 4.41 ms                                                        | 4.89 ms: 1.11x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 250 ms: 2.09x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.08x faster                                                    |
| mdp                              | 1.06 sec                                                       | 543 ms: 1.95x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                    |
| k_core                           | 1.46 sec                                                       | 953 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 12.9 us: 1.28x faster                                                   |
| go                               | 72.6 ms                                                        | 57.1 ms: 1.27x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.13x faster                                                   |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.79 ms: 1.10x faster                                                   |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 916 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.97 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| regex_v8                         | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 943 us: 1.05x faster                                                    |
| float                            | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.9 ms: 1.05x faster                                                   |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.8 ms: 1.03x faster                                                   |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.7 us: 1.03x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.5 ms: 1.03x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.3 ms: 1.02x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 98.5 us: 1.01x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.83 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 62.8 ms: 1.01x slower                                                   |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.02x slower                                                  |
| regex_compile                    | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                   |
| thrift                           | 309 us                                                         | 316 us: 1.02x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.9 ms: 1.02x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.83 ms: 1.02x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 330 ms: 1.02x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 666 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.09 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.5 ms: 1.03x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.03x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 427 us: 1.04x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.7 ms: 1.04x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.55 us: 1.04x slower                                                   |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.2 ms: 1.05x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.05x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.4 ms: 1.05x slower                                                   |
| pycparser                        | 470 ms                                                         | 496 ms: 1.06x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.31 ms: 1.06x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.55 ms: 1.07x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 133 ms: 1.08x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.7 ms: 1.08x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.6 ms: 1.08x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.94 ms: 1.09x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.6 ms: 1.09x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.89 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.3 ms: 1.11x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.6 ms: 1.12x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.63 us: 1.12x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 48.3 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.0 ms: 1.14x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.0 ms: 1.15x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| many_optionals                   | 200 us                                                         | 327 us: 1.63x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.5 ms: 2.80x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.8 ms: 3.00x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (8): fannkuch, spectral_norm, sympy_integrate, scimark_monte_carlo, genshi_text, sqlite_synth, sphinx, logging_silent
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.017x faster

# HPT report

- Reliability score: 77.33% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x