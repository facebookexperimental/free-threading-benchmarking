# Results vs. 3.12.6

- fork: python
- ref: d783d7b51d31db568de6
- machine: darwin-arm64
- commit hash: d783d7b
- commit date: 2025-03-18
- overall geometric mean: 1.074x faster
- HPT reliability: 99.95%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.01x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                   |
| html5lib       | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                    |
| sphinx         | 434 ms                                                   | 417 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 260 ms: 1.90x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 263 ms: 1.83x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 263 ms: 1.74x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 265 ms: 1.68x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.57x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.57x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 154 ms: 1.50x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 155 ms: 1.43x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.25x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 116 ms: 1.14x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 43.4 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 137 ms: 1.21x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 90.4 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.7 ms: 1.16x faster                                                    |
| nbody          | 54.2 ms                                                  | 50.4 ms: 1.08x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 48.8 ms: 1.12x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.6 ms: 1.08x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.0 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|---------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                    |
| xml_etree_parse     | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                    |
| tomli_loads         | 957 ms                                                   | 869 ms: 1.10x faster                                                     |
| xml_etree_generate  | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| xml_etree_process   | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| pickle_pure_python  | 139 us                                                   | 145 us: 1.04x slower                                                     |
| json_loads          | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| json_dumps          | 4.26 ms                                                  | 5.06 ms: 1.19x slower                                                    |
| Geometric mean      | (ref)                                                    | 1.02x faster                                                             |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.62 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.40 ms: 1.12x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 21.7 ms: 1.00x faster                                                    |
| mako            | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.69 ms: 2.39x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 260 ms: 1.90x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 263 ms: 1.83x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 263 ms: 1.74x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 265 ms: 1.68x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.57x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.57x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 154 ms: 1.50x faster                                                     |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 155 ms: 1.43x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 7.78 us: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.25x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.5 ms: 1.21x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.4 ms: 1.19x faster                                                    |
| go                               | 70.0 ms                                                  | 59.1 ms: 1.19x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| raytrace                         | 145 ms                                                   | 125 ms: 1.16x faster                                                     |
| k_core                           | 1.12 sec                                                 | 964 ms: 1.16x faster                                                     |
| float                            | 37.9 ms                                                  | 32.7 ms: 1.16x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.5 ns: 1.14x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 116 ms: 1.14x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.3 ms: 1.12x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.8 ms: 1.12x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 49.1 ms: 1.11x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 869 ms: 1.10x faster                                                     |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.58 ms: 1.10x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.3 ms: 1.09x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.92 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.08 sec: 1.08x faster                                                   |
| nbody                            | 54.2 ms                                                  | 50.4 ms: 1.08x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.39 us: 1.08x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 92.6 ms: 1.08x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 133 ms: 1.07x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.62 us: 1.07x faster                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 37.6 ms: 1.06x faster                                                    |
| pyflate                          | 216 ms                                                   | 206 ms: 1.05x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 43.4 ms: 1.05x faster                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 44.9 ms: 1.04x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 68.2 us: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| sphinx                           | 434 ms                                                   | 417 ms: 1.04x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 49.8 ms: 1.03x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.2 ms: 1.02x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.97 ms: 1.02x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.3 ms: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 949 ns: 1.02x faster                                                     |
| thrift                           | 322 us                                                   | 316 us: 1.02x faster                                                     |
| sympy_str                        | 104 ms                                                   | 103 ms: 1.02x faster                                                     |
| 2to3                             | 114 ms                                                   | 112 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 31.9 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.7 ms: 1.00x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 329 ms: 1.00x slower                                                     |
| shortest_path                    | 219 ms                                                   | 220 ms: 1.00x slower                                                     |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 43.7 ms: 1.01x slower                                                    |
| richards                         | 22.4 ms                                                  | 22.6 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| connected_components             | 201 ms                                                   | 204 ms: 1.02x slower                                                     |
| mdp                              | 1.09 sec                                                 | 1.11 sec: 1.02x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.18 ms: 1.02x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.28 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.02x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 172 ms: 1.03x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 432 us: 1.03x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 40.2 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.5 ms: 1.04x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.0 ms: 1.05x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.11 ms: 1.05x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.62 ms: 1.08x slower                                                    |
| fannkuch                         | 176 ms                                                   | 190 ms: 1.08x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 906 us: 1.09x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.40 ms: 1.12x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 5.06 ms: 1.19x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.0 ms: 1.19x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.13 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 236 us: 1.21x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 137 ms: 1.21x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 90.4 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                             |

Benchmark hidden because not significant (5): pycparser, richards_super, pprint_pformat, genshi_text, unpickle_pure_python
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250318-3.14.0a6+-d783d7b/bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.074x faster

# HPT report

- Reliability score: 99.95% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.12x