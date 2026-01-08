# Results vs. 3.13.0rc2

- fork: python
- ref: f11f5ebfe6614de23918
- machine: darwin-arm64
- commit hash: f11f5eb
- commit date: 2026-01-07
- overall geometric mean: 1.078x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3+-f11f5eb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                    |
| sphinx         | 409 ms                                                         | 396 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3+-f11f5eb |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.37x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 227 ms: 2.31x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 235 ms: 1.64x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.11x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.2 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.4 ms: 2.74x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3+-f11f5eb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.0 ms: 1.17x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.00x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.6 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3+-f11f5eb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.73 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.7 ms: 1.05x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.1 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3+-f11f5eb |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.88 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 844 ms: 1.18x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.2 ms: 1.18x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.4 ms: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.02x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3+-f11f5eb |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.89 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.40 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3+-f11f5eb |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.59 ms: 1.04x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| mako            | 4.41 ms                                                        | 4.75 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3+-f11f5eb |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.37x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 227 ms: 2.31x faster                                                     |
| mdp                              | 1.06 sec                                                       | 544 ms: 1.94x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 235 ms: 1.64x faster                                                     |
| k_core                           | 1.46 sec                                                       | 902 ms: 1.62x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.03 ms: 1.55x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                    |
| deepcopy                         | 145 us                                                         | 103 us: 1.41x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.37x faster                                                     |
| go                               | 72.6 ms                                                        | 53.3 ms: 1.36x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.4 ms: 1.30x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.22x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.88 ms: 1.20x faster                                                    |
| pyflate                          | 222 ms                                                         | 187 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 844 ms: 1.18x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.2 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| float                            | 31.4 ms                                                        | 27.0 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.11x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.73 ms: 1.10x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.1 ms: 1.10x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.6 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.5 ms: 1.09x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.83 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.2 ms: 1.08x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 930 us: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 304 ms: 1.06x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 615 ms: 1.06x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 117 ms: 1.05x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 45.7 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.04x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.4 ms: 1.04x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.59 ms: 1.04x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.5 us: 1.03x faster                                                    |
| sphinx                           | 409 ms                                                         | 396 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.76 ms: 1.03x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.75 ms: 1.02x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                    |
| thrift                           | 309 us                                                         | 304 us: 1.02x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 43.3 ms: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| pycparser                        | 470 ms                                                         | 465 ms: 1.01x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.45 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 207 ms: 1.01x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.43 us: 1.01x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.00x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.00x faster                                                     |
| deltablue                        | 1.45 ms                                                        | 1.45 ms: 1.00x slower                                                    |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 96.1 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.3 ns: 1.02x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.02x slower                                                     |
| sqlite_synth                     | 948 ns                                                         | 967 ns: 1.02x slower                                                     |
| coverage                         | 31.2 ms                                                        | 31.9 ms: 1.02x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.9 ms: 1.03x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.3 ms: 1.03x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.89 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.3 ms: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.10 us: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.8 ms: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 431 us: 1.05x slower                                                     |
| nbody                            | 42.5 ms                                                        | 44.6 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.4 ms: 1.06x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.40 ms: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.75 ms: 1.08x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.09x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 36.6 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.17x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.3 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 253 us: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.4 ms: 2.74x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (1): json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260107-3.15.0a3+-f11f5eb/bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3+-f11f5eb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.078x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.18x