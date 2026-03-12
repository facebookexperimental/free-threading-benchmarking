# Results vs. 3.13.0rc2

- fork: python
- ref: d19de375a204c74ab5f3
- machine: darwin-arm64
- commit hash: d19de37
- commit date: 2026-03-11
- overall geometric mean: 1.024x faster
- HPT reliability: 50.23%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.08x slower                                                     |
| docutils       | 1.05 sec                                                       | 987 ms: 1.06x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| sphinx         | 409 ms                                                         | 420 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 238 ms: 2.19x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 236 ms: 1.71x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.1 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.9 ms: 3.18x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.9 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.4 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 50.3 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.86 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 851 ms: 1.18x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 105 us: 1.06x slower                                                     |
| xml_etree_process    | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.91 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.23 ms: 1.22x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| mako            | 4.41 ms                                                        | 5.57 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 800 us: 2.55x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 238 ms: 2.19x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 504 us: 1.97x faster                                                     |
| mdp                              | 1.06 sec                                                       | 603 ms: 1.75x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 236 ms: 1.71x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.03 ms: 1.55x faster                                                    |
| k_core                           | 1.46 sec                                                       | 987 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 105 us: 1.38x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.31x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| go                               | 72.6 ms                                                        | 59.1 ms: 1.23x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.86 ms: 1.20x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 787 ns: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 851 ms: 1.18x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                    |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.7 ms: 1.15x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                    |
| docutils                         | 1.05 sec                                                       | 987 ms: 1.06x faster                                                     |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| pycparser                        | 470 ms                                                         | 455 ms: 1.03x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.4 ms: 1.01x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.02x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                                     |
| sphinx                           | 409 ms                                                         | 420 ms: 1.03x slower                                                     |
| richards                         | 22.1 ms                                                        | 22.8 ms: 1.03x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 670 ms: 1.03x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.34 us: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.3 ms: 1.05x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.9 ms: 1.05x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 105 us: 1.06x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.1 ms: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.10 ms: 1.08x slower                                                    |
| 2to3                             | 112 ms                                                         | 120 ms: 1.08x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 44.2 ns: 1.09x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.7 ms: 1.09x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.13 ms: 1.10x slower                                                    |
| thrift                           | 309 us                                                         | 340 us: 1.10x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.1 ms: 1.11x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.0 ms: 1.11x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 118 ms: 1.11x slower                                                     |
| shortest_path                    | 225 ms                                                         | 252 ms: 1.12x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 72.8 us: 1.13x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.1 ms: 1.14x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.91 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.5 ms: 1.16x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.9 ms: 1.16x slower                                                    |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.18x slower                                                     |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.13 ms: 1.20x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.19 us: 1.20x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.23 ms: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.6 ms: 1.23x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.6 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.57 ms: 1.26x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 43.0 ms: 1.28x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.1 ms: 1.28x slower                                                    |
| many_optionals                   | 200 us                                                         | 262 us: 1.31x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 56.2 ms: 1.31x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.9 ms: 1.34x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 584 us: 1.42x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.9 ms: 3.18x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (2): xml_etree_parse, json
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: asyncio_websockets, chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260311-3.15.0a7+-d19de37-NOGIL/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.024x faster

# HPT report

- Reliability score: 50.23% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.32x