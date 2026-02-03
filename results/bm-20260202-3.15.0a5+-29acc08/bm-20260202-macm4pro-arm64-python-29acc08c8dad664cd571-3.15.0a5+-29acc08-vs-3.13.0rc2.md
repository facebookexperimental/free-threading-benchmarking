# Results vs. 3.13.0rc2

- fork: python
- ref: 29acc08c8dad664cd571
- machine: darwin-arm64
- commit hash: 29acc08
- commit date: 2026-02-02
- overall geometric mean: 1.108x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 108 ms: 1.04x faster                                                     |
| docutils       | 1.05 sec                                                       | 979 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 20.8 ms: 1.11x faster                                                    |
| sphinx         | 409 ms                                                         | 380 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 211 ms: 2.47x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 213 ms: 2.47x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 221 ms: 1.74x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.1 ms: 1.44x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 94.5 ms: 1.40x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.39x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 242 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 247 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                     |
| async_generators                 | 193 ms                                                         | 167 ms: 1.16x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 38.8 ms: 1.11x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 181 ms: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 211 ms: 1.07x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 117 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.3 ms: 2.67x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.5 ms: 1.14x faster                                                    |
| pidigits       | 166 ms                                                         | 156 ms: 1.07x faster                                                     |
| nbody          | 42.5 ms                                                        | 43.7 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.14x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 44.5 ms: 1.08x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 92.3 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.74 ms: 1.24x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 37.3 ms: 1.24x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 818 ms: 1.22x faster                                                     |
| xml_etree_process    | 25.4 ms                                                        | 23.8 ms: 1.06x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 33.7 ms: 1.06x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.0 ms: 1.06x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 94.8 us: 1.05x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.3 us: 1.05x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 136 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.10x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.49 ms: 1.05x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.5 ms: 1.04x faster                                                    |
| mako            | 4.41 ms                                                        | 4.59 ms: 1.04x slower                                                    |
| django_template | 12.5 ms                                                        | 14.3 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 211 ms: 2.47x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 213 ms: 2.47x faster                                                     |
| mdp                              | 1.06 sec                                                       | 526 ms: 2.01x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 221 ms: 1.74x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.83 ms: 1.64x faster                                                    |
| k_core                           | 1.46 sec                                                       | 897 ms: 1.63x faster                                                     |
| deepcopy                         | 145 us                                                         | 95.2 us: 1.52x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.1 us: 1.49x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.1 ms: 1.44x faster                                                    |
| go                               | 72.6 ms                                                        | 51.4 ms: 1.41x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 94.5 ms: 1.40x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.39x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.37x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.0 ms: 1.31x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.04 us: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 242 ms: 1.25x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.74 ms: 1.24x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.3 ms: 1.24x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 818 ms: 1.22x faster                                                     |
| pyflate                          | 222 ms                                                         | 186 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 247 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                     |
| async_generators                 | 193 ms                                                         | 167 ms: 1.16x faster                                                     |
| float                            | 31.4 ms                                                        | 27.5 ms: 1.14x faster                                                    |
| richards                         | 22.1 ms                                                        | 19.3 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.14x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 21.9 ms: 1.13x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 882 us: 1.13x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.11x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 38.8 ms: 1.11x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 20.8 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.82 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                                    |
| sphinx                           | 409 ms                                                         | 380 ms: 1.08x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 44.5 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 181 ms: 1.07x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 300 ms: 1.07x faster                                                     |
| fannkuch                         | 179 ms                                                         | 167 ms: 1.07x faster                                                     |
| docutils                         | 1.05 sec                                                       | 979 ms: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                    |
| pidigits                         | 166 ms                                                         | 156 ms: 1.07x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 211 ms: 1.07x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 609 ms: 1.07x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.67 ms: 1.06x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 23.8 ms: 1.06x faster                                                    |
| json                             | 1.94 ms                                                        | 1.83 ms: 1.06x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 33.7 ms: 1.06x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.0 ms: 1.06x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 61.3 us: 1.05x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.49 ms: 1.05x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 94.8 us: 1.05x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.3 us: 1.05x faster                                                    |
| pycparser                        | 470 ms                                                         | 450 ms: 1.05x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 1.96 ms: 1.04x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 20.5 ms: 1.04x faster                                                    |
| thrift                           | 309 us                                                         | 297 us: 1.04x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.25 ms: 1.04x faster                                                    |
| 2to3                             | 112 ms                                                         | 108 ms: 1.04x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 39.5 ns: 1.03x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.41 ms: 1.03x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 92.3 ms: 1.03x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 47.1 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 205 ms: 1.01x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 122 ms: 1.01x faster                                                     |
| nqueens                          | 37.2 ms                                                        | 37.1 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                     |
| python_startup                   | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.0 ms: 1.01x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.91 us: 1.02x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 53.4 ms: 1.02x slower                                                    |
| nbody                            | 42.5 ms                                                        | 43.7 ms: 1.03x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.4 ms: 1.03x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.1 ms: 1.03x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.59 ms: 1.04x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 44.5 ms: 1.04x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 136 us: 1.04x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                     |
| raytrace                         | 109 ms                                                         | 114 ms: 1.04x slower                                                     |
| pylint                           | 106 ms                                                         | 110 ms: 1.05x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.89 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 36.6 ms: 1.09x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.8 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 117 ms: 1.14x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 43.2 ms: 1.14x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.3 ms: 1.15x slower                                                    |
| many_optionals                   | 200 us                                                         | 237 us: 1.18x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.3 ms: 2.67x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                             |

Benchmark hidden because not significant (2): sqlite_synth, coverage
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260202-3.15.0a5+-29acc08/bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.108x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.18x