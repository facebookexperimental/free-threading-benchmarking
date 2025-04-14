# Results vs. 3.13.0rc2

- fork: python
- ref: 4d3ad0467e5cb145b1f4
- machine: darwin-arm64
- commit hash: 4d3ad04
- commit date: 2025-04-13
- overall geometric mean: 1.028x faster
- HPT reliability: 60.25%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| docutils       | 1.05 sec                                                       | 989 ms: 1.06x faster                                                     |
| html5lib       | 23.1 ms                                                        | 23.0 ms: 1.00x faster                                                    |
| sphinx         | 409 ms                                                         | 416 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.07x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 85.0 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 230 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 240 ms: 1.23x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 223 ms: 1.07x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.7 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 52.9 ms: 1.24x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.80 ms: 1.09x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 100 ms: 1.06x slower                                                     |
| regex_compile  | 47.9 ms                                                        | 53.2 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 36.1 ms: 1.28x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 56.9 ms: 1.10x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 950 ms: 1.05x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 36.3 ms: 1.01x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 104 us: 1.05x slower                                                     |
| json_dumps           | 4.65 ms                                                        | 5.02 ms: 1.08x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.9 us: 1.10x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 150 us: 1.16x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.54 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.58 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.19x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.0 ms: 1.10x slower                                                    |
| mako            | 4.41 ms                                                        | 5.43 ms: 1.23x slower                                                    |
| django_template | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.18x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 753 us: 2.71x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 449 us: 2.21x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.07x faster                                                     |
| mdp                              | 1.06 sec                                                       | 562 ms: 1.88x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 85.0 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                     |
| k_core                           | 1.46 sec                                                       | 975 ms: 1.50x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 230 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.1 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 240 ms: 1.23x faster                                                     |
| deepcopy                         | 145 us                                                         | 121 us: 1.20x faster                                                     |
| go                               | 72.6 ms                                                        | 61.5 ms: 1.18x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.0 ms: 1.16x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 818 ns: 1.16x faster                                                     |
| float                            | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 14.6 us: 1.13x faster                                                    |
| pyflate                          | 222 ms                                                         | 201 ms: 1.11x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 56.9 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.80 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 989 ms: 1.06x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 950 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.26 us: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| pycparser                        | 470 ms                                                         | 464 ms: 1.01x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 23.0 ms: 1.00x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.3 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 416 ms: 1.02x slower                                                     |
| shortest_path                    | 225 ms                                                         | 230 ms: 1.02x slower                                                     |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.03x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 104 us: 1.05x slower                                                     |
| connected_components             | 208 ms                                                         | 218 ms: 1.05x slower                                                     |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                     |
| fannkuch                         | 179 ms                                                         | 189 ms: 1.06x slower                                                     |
| telco                            | 3.07 ms                                                        | 3.24 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.99 ms: 1.06x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 100 ms: 1.06x slower                                                     |
| 2to3                             | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 39.7 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 223 ms: 1.07x slower                                                     |
| json_dumps                       | 4.65 ms                                                        | 5.02 ms: 1.08x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.08 ms: 1.08x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.0 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.0 ms: 1.10x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.9 us: 1.10x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.54 ms: 1.11x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 41.8 ms: 1.11x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 357 ms: 1.11x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 53.2 ms: 1.11x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.5 ms: 1.11x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.51 us: 1.12x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 72.5 us: 1.12x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 730 ms: 1.12x slower                                                     |
| sqlalchemy_declarative           | 44.4 ms                                                        | 49.9 ms: 1.12x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 49.2 ms: 1.13x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 140 ms: 1.13x slower                                                     |
| generators                       | 15.7 ms                                                        | 17.8 ms: 1.14x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.78 us: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 54.9 ms: 1.15x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.73 ms: 1.15x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.3 ms: 1.15x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 150 us: 1.16x slower                                                     |
| chaos                            | 24.3 ms                                                        | 28.1 ms: 1.16x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.17x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 47.6 ns: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.17x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.10 ms: 1.18x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 40.2 ms: 1.19x slower                                                    |
| many_optionals                   | 200 us                                                         | 239 us: 1.19x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.36 us: 1.23x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.43 ms: 1.23x slower                                                    |
| nbody                            | 42.5 ms                                                        | 52.9 ms: 1.24x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 53.5 ms: 1.25x slower                                                    |
| coverage                         | 31.2 ms                                                        | 39.2 ms: 1.26x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.58 ms: 1.27x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 570 us: 1.38x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.67 ms: 1.39x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.7 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250413-3.14.0a7+-4d3ad04-NOGIL/bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.028x faster

# HPT report

- Reliability score: 60.25% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.17x