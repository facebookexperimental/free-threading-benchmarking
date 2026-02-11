# Results vs. 3.13.0rc2

- fork: python
- ref: d18dbd5e1ce6ca43b559
- machine: darwin-arm64
- commit hash: d18dbd5
- commit date: 2026-02-10
- overall geometric mean: 1.087x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.1 ms: 1.10x faster                                                    |
| sphinx         | 409 ms                                                         | 389 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 220 ms: 2.39x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.35x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 225 ms: 1.71x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 96.5 ms: 1.37x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 250 ms: 1.21x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.98 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.9 ms: 2.73x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.5 ms: 1.14x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.2 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 44.9 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 834 ms: 1.20x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.5 ms: 1.05x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 95.9 us: 1.04x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 138 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.73 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.30 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.53 ms: 1.05x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| mako            | 4.41 ms                                                        | 4.58 ms: 1.04x slower                                                    |
| django_template | 12.5 ms                                                        | 14.5 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 220 ms: 2.39x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.35x faster                                                     |
| mdp                              | 1.06 sec                                                       | 531 ms: 1.99x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 225 ms: 1.71x faster                                                     |
| k_core                           | 1.46 sec                                                       | 896 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.96 ms: 1.58x faster                                                    |
| deepcopy                         | 145 us                                                         | 97.0 us: 1.50x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.2 us: 1.46x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.38x faster                                                     |
| go                               | 72.6 ms                                                        | 52.6 ms: 1.38x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 96.5 ms: 1.37x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.34x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.2 ms: 1.30x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.22x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 250 ms: 1.21x faster                                                     |
| pyflate                          | 222 ms                                                         | 184 ms: 1.21x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 834 ms: 1.20x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                     |
| float                            | 31.4 ms                                                        | 27.5 ms: 1.14x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                    |
| richards                         | 22.1 ms                                                        | 19.9 ms: 1.11x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.3 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.79 ms: 1.10x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.1 ms: 1.10x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 912 us: 1.09x faster                                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.98 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 44.9 ms: 1.07x faster                                                    |
| fannkuch                         | 179 ms                                                         | 168 ms: 1.06x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 118 ms: 1.05x faster                                                     |
| sphinx                           | 409 ms                                                         | 389 ms: 1.05x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 59.5 ms: 1.05x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.53 ms: 1.05x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 308 ms: 1.05x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 624 ms: 1.04x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.74 ms: 1.04x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 95.9 us: 1.04x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                    |
| pycparser                        | 470 ms                                                         | 458 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.36 ms: 1.02x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.19 us: 1.02x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.6 us: 1.02x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 933 ns: 1.02x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.41 us: 1.02x faster                                                    |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.77 ms: 1.00x faster                                                    |
| 2to3                             | 112 ms                                                         | 112 ms: 1.01x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.73 ms: 1.01x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.2 ns: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.9 ms: 1.02x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.99 us: 1.03x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.4 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.2 ms: 1.03x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.58 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.1 ms: 1.04x slower                                                    |
| nbody                            | 42.5 ms                                                        | 44.2 ms: 1.04x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 54.5 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                     |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 45.0 ms: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.30 ms: 1.06x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 138 us: 1.06x slower                                                     |
| chaos                            | 24.3 ms                                                        | 25.8 ms: 1.06x slower                                                    |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.7 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.3 ms: 1.16x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.5 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.0 ms: 1.19x slower                                                    |
| many_optionals                   | 200 us                                                         | 251 us: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.9 ms: 2.73x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (5): thrift, regex_dna, spectral_norm, deltablue, gc_traversal
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260210-3.15.0a5+-d18dbd5/bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.087x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.18x