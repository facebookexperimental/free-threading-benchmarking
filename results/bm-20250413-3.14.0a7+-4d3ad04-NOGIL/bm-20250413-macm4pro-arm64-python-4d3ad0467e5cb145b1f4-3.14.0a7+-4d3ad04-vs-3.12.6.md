# Results vs. 3.12.6

- fork: python
- ref: 4d3ad0467e5cb145b1f4
- machine: darwin-arm64
- commit hash: 4d3ad04
- commit date: 2025-04-13
- overall geometric mean: 1.108x faster
- HPT reliability: 99.40%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.04x slower                                                     |
| docutils       | 1.02 sec                                                 | 989 ms: 1.03x faster                                                     |
| sphinx         | 434 ms                                                   | 416 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.45x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.29x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.0 ms: 2.03x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.88x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.77x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 230 ms: 1.47x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 223 ms: 1.05x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 50.2 ms: 1.10x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.7 ms: 2.42x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.39x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| nbody          | 54.2 ms                                                  | 52.9 ms: 1.03x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.12x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 53.2 ms: 1.03x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 100 ms: 1.01x slower                                                     |
| regex_v8       | 9.59 ms                                                  | 9.80 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 36.1 ms: 1.43x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.9 ms: 1.19x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.3 ms: 1.07x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 104 us: 1.01x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 150 us: 1.08x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.9 us: 1.10x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.02 ms: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                             |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.54 ms: 1.19x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.58 ms: 1.33x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.26x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 23.4 ms: 1.07x slower                                                    |
| mako            | 4.77 ms                                                  | 5.43 ms: 1.14x slower                                                    |
| django_template | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 753 us: 2.67x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.45x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 8.67 ms: 2.39x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.29x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.0 ms: 2.03x faster                                                    |
| mdp                              | 1.09 sec                                                 | 562 ms: 1.94x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.88x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 449 us: 1.85x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.77x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 230 ms: 1.47x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.1 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                     |
| float                            | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| deepcopy                         | 161 us                                                   | 121 us: 1.33x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 14.6 us: 1.25x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.8 ms: 1.23x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 56.9 ms: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 818 ns: 1.18x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.36 us: 1.18x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| pylint                           | 128 ms                                                   | 111 ms: 1.15x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                    |
| k_core                           | 1.12 sec                                                 | 975 ms: 1.15x faster                                                     |
| go                               | 70.0 ms                                                  | 61.5 ms: 1.14x faster                                                    |
| raytrace                         | 145 ms                                                   | 128 ms: 1.13x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.0 ms: 1.11x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 49.2 ms: 1.10x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.7 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 201 ms: 1.08x faster                                                     |
| pycparser                        | 497 ms                                                   | 464 ms: 1.07x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 36.3 ms: 1.07x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 47.6 ns: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                     |
| sphinx                           | 434 ms                                                   | 416 ms: 1.04x faster                                                     |
| docutils                         | 1.02 sec                                                 | 989 ms: 1.03x faster                                                     |
| chaos                            | 28.9 ms                                                  | 28.1 ms: 1.03x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.51 us: 1.03x faster                                                    |
| nbody                            | 54.2 ms                                                  | 52.9 ms: 1.03x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.2 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 140 ms: 1.01x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.78 us: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.99 ms: 1.00x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 100 ms: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 104 us: 1.01x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.10 ms: 1.01x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.08 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.5 us: 1.02x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.80 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 40.2 ms: 1.03x slower                                                    |
| 2to3                             | 114 ms                                                   | 118 ms: 1.04x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 53.5 ms: 1.04x slower                                                    |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.3 ms: 1.05x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.8 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 223 ms: 1.05x slower                                                     |
| shortest_path                    | 219 ms                                                   | 230 ms: 1.05x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 41.8 ms: 1.05x slower                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 49.9 ms: 1.07x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.0 ms: 1.07x slower                                                    |
| fannkuch                         | 176 ms                                                   | 189 ms: 1.07x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.4 ms: 1.07x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 150 us: 1.08x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 27.5 ms: 1.08x slower                                                    |
| connected_components             | 201 ms                                                   | 218 ms: 1.08x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 357 ms: 1.09x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 730 ms: 1.10x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.9 us: 1.10x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 50.2 ms: 1.10x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.73 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.43 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.9 ms: 1.15x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.02 ms: 1.18x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.54 ms: 1.19x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                    |
| many_optionals                   | 195 us                                                   | 239 us: 1.23x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.24 ms: 1.24x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.58 ms: 1.33x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 570 us: 1.36x slower                                                     |
| coverage                         | 26.9 ms                                                  | 39.2 ms: 1.46x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.7 ms: 2.42x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (3): tomli_loads, async_tree_eager_memoization_tg, html5lib
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250413-3.14.0a7+-4d3ad04-NOGIL/bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.108x faster

# HPT report

- Reliability score: 99.40% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.22x