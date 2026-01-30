# Results vs. 3.13.0rc2

- fork: python
- ref: 5f57f6970bdea45cc2b1
- machine: darwin-arm64
- commit hash: 5f57f69
- commit date: 2026-01-30
- overall geometric mean: 1.113x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 107 ms: 1.04x faster                                                     |
| docutils       | 1.05 sec                                                       | 975 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 20.6 ms: 1.12x faster                                                    |
| sphinx         | 409 ms                                                         | 378 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                          | 1.08x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 212 ms: 2.48x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 211 ms: 2.46x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 219 ms: 1.85x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 220 ms: 1.75x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 98.5 ms: 1.44x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 132 ms: 1.41x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 93.9 ms: 1.41x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 240 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                     |
| async_generators                 | 193 ms                                                         | 167 ms: 1.16x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 38.7 ms: 1.12x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.90 ms: 1.09x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 180 ms: 1.07x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 211 ms: 1.07x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 116 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.8 ms: 2.65x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.0 ms: 1.17x faster                                                    |
| pidigits       | 166 ms                                                         | 155 ms: 1.07x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.4 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.40 ms: 1.14x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 43.8 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 91.9 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.10x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.77 ms: 1.24x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 817 ms: 1.22x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 37.8 ms: 1.22x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.9 ms: 1.06x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 33.8 ms: 1.06x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.3 us: 1.05x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 95.7 us: 1.04x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 135 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.09x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.62 ms: 1.00x faster                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.45 ms: 1.06x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.6 ms: 1.04x faster                                                    |
| mako            | 4.41 ms                                                        | 4.54 ms: 1.03x slower                                                    |
| django_template | 12.5 ms                                                        | 14.3 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 212 ms: 2.48x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 211 ms: 2.46x faster                                                     |
| mdp                              | 1.06 sec                                                       | 525 ms: 2.01x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 219 ms: 1.85x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 220 ms: 1.75x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.79 ms: 1.65x faster                                                    |
| k_core                           | 1.46 sec                                                       | 894 ms: 1.64x faster                                                     |
| deepcopy                         | 145 us                                                         | 94.5 us: 1.54x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.0 us: 1.50x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 98.5 ms: 1.44x faster                                                    |
| go                               | 72.6 ms                                                        | 51.0 ms: 1.42x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 132 ms: 1.41x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 93.9 ms: 1.41x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.37x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 48.3 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 240 ms: 1.25x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.04 us: 1.25x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.77 ms: 1.24x faster                                                    |
| pyflate                          | 222 ms                                                         | 181 ms: 1.23x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 817 ms: 1.22x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.8 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                     |
| float                            | 31.4 ms                                                        | 27.0 ms: 1.17x faster                                                    |
| async_generators                 | 193 ms                                                         | 167 ms: 1.16x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 866 us: 1.15x faster                                                     |
| richards                         | 22.1 ms                                                        | 19.4 ms: 1.14x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.40 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 21.9 ms: 1.13x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 20.6 ms: 1.12x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.7 ms: 1.12x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 38.7 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.11x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.1 ms: 1.10x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 43.8 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.90 ms: 1.09x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.83 ms: 1.08x faster                                                    |
| sphinx                           | 409 ms                                                         | 378 ms: 1.08x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 299 ms: 1.08x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 180 ms: 1.07x faster                                                     |
| docutils                         | 1.05 sec                                                       | 975 ms: 1.07x faster                                                     |
| fannkuch                         | 179 ms                                                         | 166 ms: 1.07x faster                                                     |
| json                             | 1.94 ms                                                        | 1.81 ms: 1.07x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.07x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 607 ms: 1.07x faster                                                     |
| pidigits                         | 166 ms                                                         | 155 ms: 1.07x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 211 ms: 1.07x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 60.7 us: 1.06x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 23.9 ms: 1.06x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 33.8 ms: 1.06x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.69 ms: 1.06x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.45 ms: 1.06x faster                                                    |
| pycparser                        | 470 ms                                                         | 445 ms: 1.06x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.3 us: 1.05x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.13 us: 1.05x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 1.95 ms: 1.05x faster                                                    |
| 2to3                             | 112 ms                                                         | 107 ms: 1.04x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.34 us: 1.04x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.22 ms: 1.04x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 95.7 us: 1.04x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 20.6 ms: 1.04x faster                                                    |
| thrift                           | 309 us                                                         | 298 us: 1.04x faster                                                     |
| deltablue                        | 1.45 ms                                                        | 1.40 ms: 1.03x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 91.9 ms: 1.03x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 47.2 ms: 1.01x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 40.2 ns: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 940 ns: 1.01x faster                                                     |
| nqueens                          | 37.2 ms                                                        | 37.0 ms: 1.01x faster                                                    |
| coverage                         | 31.2 ms                                                        | 31.0 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 43.6 ms: 1.00x faster                                                    |
| connected_components             | 208 ms                                                         | 207 ms: 1.00x faster                                                     |
| python_startup                   | 8.63 ms                                                        | 8.62 ms: 1.00x faster                                                    |
| comprehensions                   | 6.80 us                                                        | 6.84 us: 1.01x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 43.7 ms: 1.02x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 53.5 ms: 1.02x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 97.8 ms: 1.02x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.54 ms: 1.03x slower                                                    |
| raytrace                         | 109 ms                                                         | 112 ms: 1.03x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 165 ms: 1.04x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 135 us: 1.04x slower                                                     |
| chaos                            | 24.3 ms                                                        | 25.2 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                     |
| pylint                           | 106 ms                                                         | 110 ms: 1.04x slower                                                     |
| nbody                            | 42.5 ms                                                        | 44.4 ms: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 36.4 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                     |
| generators                       | 15.7 ms                                                        | 17.7 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 116 ms: 1.13x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 43.1 ms: 1.14x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.3 ms: 1.15x slower                                                    |
| many_optionals                   | 200 us                                                         | 235 us: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.8 ms: 2.65x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                             |

Benchmark hidden because not significant (2): xml_etree_parse, scimark_sparse_mat_mult
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260130-3.15.0a5+-5f57f69/bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.113x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.18x