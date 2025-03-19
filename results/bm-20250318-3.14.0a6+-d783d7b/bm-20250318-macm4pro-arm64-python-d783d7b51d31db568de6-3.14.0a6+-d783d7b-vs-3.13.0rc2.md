# Results vs. 3.13.0rc2

- fork: python
- ref: d783d7b51d31db568de6
- machine: darwin-arm64
- commit hash: d783d7b
- commit date: 2025-03-18
- overall geometric mean: 1.003x slower
- HPT reliability: 76.58%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.02x slower                                                   |
| html5lib       | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                    |
| sphinx         | 409 ms                                                         | 417 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 260 ms: 2.02x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 265 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 263 ms: 1.54x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 263 ms: 1.47x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 154 ms: 1.21x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.21x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 155 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 43.4 ms: 1.00x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 137 ms: 1.33x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 90.4 ms: 3.12x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| float          | 31.4 ms                                                        | 32.7 ms: 1.04x slower                                                    |
| nbody          | 42.5 ms                                                        | 50.4 ms: 1.19x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.0 ms: 1.06x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 92.6 ms: 1.02x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 869 ms: 1.15x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.1 ms: 1.05x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 103 us: 1.04x slower                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 37.4 ms: 1.05x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.07x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.06 ms: 1.09x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.62 ms: 1.00x faster                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.40 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.5 ms: 1.05x slower                                                    |
| mako            | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 260 ms: 2.02x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 265 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 263 ms: 1.54x faster                                                     |
| k_core                           | 1.46 sec                                                       | 964 ms: 1.52x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 263 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.28x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| go                               | 72.6 ms                                                        | 59.1 ms: 1.23x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 154 ms: 1.21x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.21x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 155 ms: 1.19x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.3 ms: 1.18x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 869 ms: 1.15x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 17.5 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 906 us: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| pyflate                          | 222 ms                                                         | 206 ms: 1.08x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 10.0 ms: 1.06x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.05x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.1 ms: 1.05x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.08 sec: 1.02x faster                                                   |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 92.6 ms: 1.02x faster                                                    |
| connected_components             | 208 ms                                                         | 204 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 37.6 ms: 1.01x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.62 ms: 1.00x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 43.4 ms: 1.00x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                    |
| 2to3                             | 112 ms                                                         | 112 ms: 1.01x slower                                                     |
| sqlalchemy_declarative           | 44.4 ms                                                        | 44.9 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.3 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 417 ms: 1.02x slower                                                     |
| telco                            | 3.07 ms                                                        | 3.13 ms: 1.02x slower                                                    |
| richards                         | 22.1 ms                                                        | 22.6 ms: 1.02x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 665 ms: 1.02x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 329 ms: 1.02x slower                                                     |
| thrift                           | 309 us                                                         | 316 us: 1.02x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.0 ms: 1.03x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.3 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.11 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 103 us: 1.04x slower                                                     |
| float                            | 31.4 ms                                                        | 32.7 ms: 1.04x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 2.97 ms: 1.04x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.4 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 432 us: 1.05x slower                                                     |
| mdp                              | 1.06 sec                                                       | 1.11 sec: 1.05x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 10.5 ms: 1.05x slower                                                    |
| pycparser                        | 470 ms                                                         | 496 ms: 1.05x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 68.2 us: 1.06x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.28 ms: 1.06x slower                                                    |
| fannkuch                         | 179 ms                                                         | 190 ms: 1.06x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.07x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 31.9 ms: 1.07x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.39 us: 1.07x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 133 ms: 1.07x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.62 us: 1.07x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.40 ms: 1.07x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 103 ms: 1.08x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.3 ms: 1.08x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 172 ms: 1.08x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.92 ms: 1.08x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.58 ms: 1.09x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.18 ms: 1.09x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.06 ms: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.5 ns: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 49.1 ms: 1.12x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.78 us: 1.14x slower                                                    |
| raytrace                         | 109 ms                                                         | 125 ms: 1.14x slower                                                     |
| chaos                            | 24.3 ms                                                        | 28.2 ms: 1.16x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 49.8 ms: 1.16x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.4 ms: 1.17x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.7 ms: 1.17x slower                                                    |
| many_optionals                   | 200 us                                                         | 236 us: 1.18x slower                                                     |
| nbody                            | 42.5 ms                                                        | 50.4 ms: 1.19x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 40.2 ms: 1.19x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 137 ms: 1.33x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.69 ms: 1.39x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 90.4 ms: 3.12x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (8) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250318-3.14.0a6+-d783d7b/bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 76.58% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.07x