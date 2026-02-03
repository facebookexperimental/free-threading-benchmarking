# Results vs. 3.13.0rc2

- fork: python
- ref: 29acc08c8dad664cd571
- machine: darwin-arm64
- commit hash: 29acc08
- commit date: 2026-02-02
- overall geometric mean: 1.041x faster
- HPT reliability: 83.37%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.05x slower                                                     |
| docutils       | 1.05 sec                                                       | 974 ms: 1.08x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 239 ms: 2.18x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 244 ms: 1.66x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 241 ms: 1.60x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 260 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 45.7 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.2 ms: 3.15x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 157 ms: 1.06x faster                                                     |
| nbody          | 42.5 ms                                                        | 55.2 ms: 1.30x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 91.2 ms: 1.04x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 36.9 ms: 1.25x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 840 ms: 1.19x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 55.8 ms: 1.12x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.02x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.6 ms: 1.02x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.2 ms: 1.03x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 104 us: 1.05x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 142 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.59 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.5 ms: 1.01x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| mako            | 4.41 ms                                                        | 5.49 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.13x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 770 us: 2.65x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 239 ms: 2.18x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 501 us: 1.98x faster                                                     |
| mdp                              | 1.06 sec                                                       | 593 ms: 1.78x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 244 ms: 1.66x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 241 ms: 1.60x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.07 ms: 1.54x faster                                                    |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 104 us: 1.39x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.2 us: 1.35x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.9 ms: 1.25x faster                                                    |
| go                               | 72.6 ms                                                        | 58.1 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.23x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 52.8 ms: 1.21x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 840 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 807 ns: 1.17x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                    |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.13 us: 1.15x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 260 ms: 1.13x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 55.8 ms: 1.12x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                   |
| docutils                         | 1.05 sec                                                       | 974 ms: 1.08x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| fannkuch                         | 179 ms                                                         | 168 ms: 1.07x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                    |
| pidigits                         | 166 ms                                                         | 157 ms: 1.06x faster                                                     |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                     |
| pycparser                        | 470 ms                                                         | 447 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 91.2 ms: 1.04x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 528 ms: 1.00x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.5 ms: 1.01x slower                                                    |
| richards                         | 22.1 ms                                                        | 22.3 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 325 ms: 1.01x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.6 ms: 1.02x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 127 ms: 1.02x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 668 ms: 1.03x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 25.4 ms: 1.03x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.2 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 104 us: 1.05x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.90 ms: 1.05x slower                                                    |
| thrift                           | 309 us                                                         | 326 us: 1.05x slower                                                     |
| 2to3                             | 112 ms                                                         | 118 ms: 1.05x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 45.7 ms: 1.06x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 68.5 us: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.3 ns: 1.07x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.62 us: 1.07x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.2 ms: 1.08x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.07 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 142 us: 1.09x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.59 ms: 1.10x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.59 ms: 1.11x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.4 ms: 1.11x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.0 ms: 1.11x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                    |
| shortest_path                    | 225 ms                                                         | 254 ms: 1.13x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 108 ms: 1.13x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 59.4 ms: 1.14x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.0 ms: 1.14x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 183 ms: 1.15x slower                                                     |
| raytrace                         | 109 ms                                                         | 125 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.08 ms: 1.17x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.03 us: 1.18x slower                                                    |
| connected_components             | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 44.9 ms: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| coverage                         | 31.2 ms                                                        | 38.5 ms: 1.24x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 41.8 ms: 1.24x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.49 ms: 1.24x slower                                                    |
| many_optionals                   | 200 us                                                         | 258 us: 1.29x slower                                                     |
| generators                       | 15.7 ms                                                        | 20.3 ms: 1.29x slower                                                    |
| nbody                            | 42.5 ms                                                        | 55.2 ms: 1.30x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 57.9 ms: 1.35x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 562 us: 1.36x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.2 ms: 3.15x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260202-3.15.0a5+-29acc08-NOGIL/bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.041x faster

# HPT report

- Reliability score: 83.37% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.30x