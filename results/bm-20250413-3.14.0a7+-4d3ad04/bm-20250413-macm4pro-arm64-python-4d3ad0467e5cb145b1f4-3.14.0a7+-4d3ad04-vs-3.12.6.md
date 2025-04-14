# Results vs. 3.12.6

- fork: python
- ref: 4d3ad0467e5cb145b1f4
- machine: darwin-arm64
- commit hash: 4d3ad04
- commit date: 2025-04-13
- overall geometric mean: 1.112x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                    |
| sphinx         | 434 ms                                                   | 408 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.01x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.84x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 255 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.65x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                     |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 42.2 ms: 1.08x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.7 ms: 2.76x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                    |
| nbody          | 54.2 ms                                                  | 48.2 ms: 1.12x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.6 ms: 1.15x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.4 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.4 ms: 1.19x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.8 ms: 1.09x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.3 ms: 1.07x faster                                                    |
| tomli_loads          | 957 ms                                                   | 898 ms: 1.07x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 25.3 ms: 1.05x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 99.4 us: 1.04x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.03x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.93 ms: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.01 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.75 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.89 ms: 1.06x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                    |
| mako            | 4.77 ms                                                  | 4.85 ms: 1.02x slower                                                    |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.77 ms: 2.37x faster                                                    |
| mdp                              | 1.09 sec                                                 | 516 ms: 2.11x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.01x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.84x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 255 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.65x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                     |
| deepcopy                         | 161 us                                                   | 107 us: 1.51x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.45x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.36x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.09 us: 1.34x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.40 us: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                     |
| float                            | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 39.9 ns: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                     |
| generators                       | 21.9 ms                                                  | 17.4 ms: 1.26x faster                                                    |
| go                               | 70.0 ms                                                  | 56.2 ms: 1.25x faster                                                    |
| raytrace                         | 145 ms                                                   | 117 ms: 1.23x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 50.3 ms: 1.21x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.6 ms: 1.21x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.4 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| k_core                           | 1.12 sec                                                 | 940 ms: 1.19x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.4 ms: 1.19x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.3 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 47.6 ms: 1.15x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.14x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.13x faster                                                     |
| nbody                            | 54.2 ms                                                  | 48.2 ms: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| pyflate                          | 216 ms                                                   | 194 ms: 1.12x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.0 ms: 1.11x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.1 us: 1.11x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 46.4 ms: 1.10x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.2 ms: 1.10x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.77 ms: 1.10x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 35.8 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.40 ms: 1.08x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.37 us: 1.08x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.2 ms: 1.08x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.3 ms: 1.07x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 898 ms: 1.07x faster                                                     |
| sympy_str                        | 104 ms                                                   | 98.2 ms: 1.06x faster                                                    |
| sphinx                           | 434 ms                                                   | 408 ms: 1.06x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 9.89 ms: 1.06x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.3 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 44.9 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.3 ms: 1.04x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.00 ms: 1.04x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 99.4 us: 1.04x faster                                                    |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.7 ms: 1.03x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 947 ns: 1.02x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 24.9 ms: 1.02x faster                                                    |
| pycparser                        | 497 ms                                                   | 489 ms: 1.02x faster                                                     |
| shortest_path                    | 219 ms                                                   | 215 ms: 1.02x faster                                                     |
| richards                         | 22.4 ms                                                  | 22.1 ms: 1.01x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.01x faster                                                     |
| connected_components             | 201 ms                                                   | 200 ms: 1.00x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.03 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.85 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 40.7 ms: 1.03x slower                                                    |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.35 ms: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.03x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 437 us: 1.04x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.9 ms: 1.04x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 891 us: 1.07x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 10.4 ms: 1.08x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.01 ms: 1.12x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.98 ms: 1.14x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.93 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.75 ms: 1.18x slower                                                    |
| many_optionals                   | 195 us                                                   | 235 us: 1.20x slower                                                     |
| coverage                         | 26.9 ms                                                  | 33.3 ms: 1.24x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.7 ms: 2.76x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (3): regex_dna, pprint_pformat, pprint_safe_repr
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250413-3.14.0a7+-4d3ad04/bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.112x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.12x