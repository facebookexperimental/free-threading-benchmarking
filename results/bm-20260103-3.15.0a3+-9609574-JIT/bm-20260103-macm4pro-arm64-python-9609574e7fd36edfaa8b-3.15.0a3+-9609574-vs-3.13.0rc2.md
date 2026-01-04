# Results vs. 3.13.0rc2

- fork: python
- ref: 9609574e7fd36edfaa8b
- machine: darwin-arm64
- commit hash: 9609574
- commit date: 2026-01-03
- overall geometric mean: 1.159x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 109 ms: 1.03x faster                                                     |
| docutils       | 1.05 sec                                                       | 999 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 19.8 ms: 1.17x faster                                                    |
| sphinx         | 409 ms                                                         | 391 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 215 ms: 2.42x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.39x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 219 ms: 1.85x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 227 ms: 1.70x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 97.5 ms: 1.46x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 96.8 ms: 1.37x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 250 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 37.5 ms: 1.15x faster                                                    |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.8 ms: 2.69x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.22x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 22.6 ms: 1.39x faster                                                    |
| nbody          | 42.5 ms                                                        | 40.0 ms: 1.06x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.15x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 40.6 ms: 1.18x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.58 ms: 1.12x faster                                                    |
| Geometric mean | (ref)                                                          | 1.11x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle_pure_python | 99.5 us                                                        | 71.7 us: 1.39x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 772 ms: 1.30x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.66 ms: 1.27x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 36.9 ms: 1.25x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 110 us: 1.19x faster                                                     |
| xml_etree_process    | 25.4 ms                                                        | 21.8 ms: 1.16x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 31.0 ms: 1.16x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.2 ms: 1.02x faster                                                    |
| Geometric mean       | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.26 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 3.89 ms: 1.13x faster                                                    |
| genshi_text     | 9.97 ms                                                        | 8.91 ms: 1.12x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                    |
| django_template | 12.5 ms                                                        | 13.7 ms: 1.10x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.04x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 215 ms: 2.42x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.39x faster                                                     |
| richards                         | 22.1 ms                                                        | 9.49 ms: 2.32x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 11.2 ms: 2.19x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 219 ms: 1.85x faster                                                     |
| mdp                              | 1.06 sec                                                       | 579 ms: 1.83x faster                                                     |
| k_core                           | 1.46 sec                                                       | 860 ms: 1.70x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 227 ms: 1.70x faster                                                     |
| go                               | 72.6 ms                                                        | 42.8 ms: 1.70x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 3.84 ms: 1.63x faster                                                    |
| pyflate                          | 222 ms                                                         | 142 ms: 1.56x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 42.1 ms: 1.52x faster                                                    |
| deepcopy                         | 145 us                                                         | 96.8 us: 1.50x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.3 us: 1.46x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 97.5 ms: 1.46x faster                                                    |
| float                            | 31.4 ms                                                        | 22.6 ms: 1.39x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 71.7 us: 1.39x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 96.8 ms: 1.37x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.0 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.35x faster                                                     |
| deltablue                        | 1.45 ms                                                        | 1.12 ms: 1.30x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1000 ns: 1.30x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 772 ms: 1.30x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.66 ms: 1.27x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 256 ms: 1.26x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 518 ms: 1.25x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.9 ms: 1.25x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 101 ms: 1.23x faster                                                     |
| logging_silent                   | 40.6 ns                                                        | 33.2 ns: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 250 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.57 ms: 1.19x faster                                                    |
| pickle_pure_python               | 130 us                                                         | 110 us: 1.19x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 40.6 ms: 1.18x faster                                                    |
| scimark_lu                       | 42.8 ms                                                        | 36.5 ms: 1.17x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 19.8 ms: 1.17x faster                                                    |
| fannkuch                         | 179 ms                                                         | 153 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 21.8 ms: 1.16x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 31.0 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.84 sec: 1.15x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 37.5 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| mako                             | 4.41 ms                                                        | 3.89 ms: 1.13x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 8.91 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.58 ms: 1.12x faster                                                    |
| chaos                            | 24.3 ms                                                        | 21.9 ms: 1.11x faster                                                    |
| comprehensions                   | 6.80 us                                                        | 6.18 us: 1.10x faster                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 30.8 ms: 1.09x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.61 ms: 1.09x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 918 us: 1.08x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 40.5 ms: 1.08x faster                                                    |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                     |
| pycparser                        | 470 ms                                                         | 438 ms: 1.07x faster                                                     |
| json                             | 1.94 ms                                                        | 1.82 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| nbody                            | 42.5 ms                                                        | 40.0 ms: 1.06x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.10 us: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 45.3 ms: 1.06x faster                                                    |
| connected_components             | 208 ms                                                         | 198 ms: 1.05x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.32 us: 1.05x faster                                                    |
| docutils                         | 1.05 sec                                                       | 999 ms: 1.05x faster                                                     |
| sphinx                           | 409 ms                                                         | 391 ms: 1.04x faster                                                     |
| shortest_path                    | 225 ms                                                         | 215 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 62.5 us: 1.03x faster                                                    |
| raytrace                         | 109 ms                                                         | 105 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| 2to3                             | 112 ms                                                         | 109 ms: 1.03x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| thrift                           | 309 us                                                         | 303 us: 1.02x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 61.2 ms: 1.02x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| python_startup                   | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 961 ns: 1.01x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 38.5 ms: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.26 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.87 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.0 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.4 ms: 1.08x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 105 ms: 1.10x slower                                                     |
| django_template                  | 12.5 ms                                                        | 13.7 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| pylint                           | 106 ms                                                         | 122 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 44.5 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.9 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 247 us: 1.23x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.8 ms: 2.69x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                             |

Benchmark hidden because not significant (3): regex_dna, sympy_integrate, gc_traversal
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260103-3.15.0a3+-9609574-JIT/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.159x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.20x