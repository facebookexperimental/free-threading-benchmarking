# Results vs. 3.13.0rc2

- fork: python
- ref: af29d5cfd19bf2656955
- machine: darwin-arm64
- commit hash: af29d5c
- commit date: 2025-03-24
- overall geometric mean: 1.044x faster
- HPT reliability: 53.64%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 978 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                    |
| sphinx         | 409 ms                                                         | 403 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 186 ms: 2.80x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 199 ms: 2.64x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 190 ms: 2.13x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 205 ms: 1.88x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 83.2 ms: 1.59x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 121 ms: 1.54x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.9 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 231 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 240 ms: 1.22x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.11 ms: 1.18x faster                                                    |
| async_generators                 | 193 ms                                                         | 169 ms: 1.14x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 222 ms: 1.07x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 110 ms: 1.07x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 74.9 ms: 2.59x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.28x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                    |
| nbody          | 42.5 ms                                                        | 60.1 ms: 1.41x slower                                                    |
| Geometric mean | (ref)                                                          | 1.09x slower                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.50 ms: 1.08x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 49.4 ms: 1.03x slower                                                    |
| regex_dna      | 94.6 ms                                                        | 103 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 35.4 ms: 1.30x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 882 ms: 1.13x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 98.8 us: 1.01x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.07x slower                                                     |
| json_loads           | 10.8 us                                                        | 11.8 us: 1.09x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.09 ms: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.31 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.35 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 20.9 ms: 1.02x faster                                                    |
| genshi_text     | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                    |
| mako            | 4.41 ms                                                        | 5.47 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 186 ms: 2.80x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 771 us: 2.65x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 199 ms: 2.64x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 464 us: 2.14x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 190 ms: 2.13x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 205 ms: 1.88x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 83.2 ms: 1.59x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 121 ms: 1.54x faster                                                     |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.45x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.9 ms: 1.42x faster                                                    |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 231 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 35.4 ms: 1.30x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.3 us: 1.24x faster                                                    |
| go                               | 72.6 ms                                                        | 58.6 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 240 ms: 1.22x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.0 ms: 1.19x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.11 ms: 1.18x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 810 ns: 1.17x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.12 us: 1.16x faster                                                    |
| async_generators                 | 193 ms                                                         | 169 ms: 1.14x faster                                                     |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 882 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| generators                       | 15.7 ms                                                        | 14.0 ms: 1.13x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                    |
| float                            | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.50 ms: 1.08x faster                                                    |
| docutils                         | 1.05 sec                                                       | 978 ms: 1.07x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| pycparser                        | 470 ms                                                         | 452 ms: 1.04x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 20.9 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| sphinx                           | 409 ms                                                         | 403 ms: 1.01x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.8 us: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 311 us: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 2.93 ms: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 49.4 ms: 1.03x slower                                                    |
| richards                         | 22.1 ms                                                        | 22.9 ms: 1.04x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.8 ms: 1.04x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.88 ms: 1.05x slower                                                    |
| mdp                              | 1.06 sec                                                       | 1.11 sec: 1.05x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 39.9 ms: 1.06x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 340 ms: 1.06x slower                                                     |
| fannkuch                         | 179 ms                                                         | 189 ms: 1.06x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 39.5 ms: 1.06x slower                                                    |
| shortest_path                    | 225 ms                                                         | 239 ms: 1.06x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 691 ms: 1.06x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.54 ms: 1.06x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.38 us: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.61 us: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 222 ms: 1.07x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 69.0 us: 1.07x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.3 ns: 1.07x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 110 ms: 1.07x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.07x slower                                                     |
| telco                            | 3.07 ms                                                        | 3.30 ms: 1.08x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.31 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.42 ms: 1.08x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 48.1 ms: 1.08x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 103 ms: 1.08x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.8 us: 1.09x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 104 ms: 1.09x slower                                                     |
| json_dumps                       | 4.65 ms                                                        | 5.09 ms: 1.09x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 57.2 ms: 1.09x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 175 ms: 1.10x slower                                                     |
| connected_components             | 208 ms                                                         | 230 ms: 1.11x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.5 ms: 1.12x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 53.7 ms: 1.12x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 139 ms: 1.12x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 49.8 ms: 1.14x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.8 ms: 1.15x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.89 us: 1.16x slower                                                    |
| many_optionals                   | 200 us                                                         | 235 us: 1.17x slower                                                     |
| raytrace                         | 109 ms                                                         | 129 ms: 1.18x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 39.9 ms: 1.19x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 51.4 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.19 ms: 1.23x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.35 ms: 1.24x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.6 ms: 1.24x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.47 ms: 1.24x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 8.44 ms: 1.35x slower                                                    |
| nbody                            | 42.5 ms                                                        | 60.1 ms: 1.41x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 590 us: 1.43x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 74.9 ms: 2.59x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (2): pidigits, pathlib
Ignored benchmarks (9) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250324-3.14.0a6+-af29d5c-CLANG,NOGIL/bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.044x faster

# HPT report

- Reliability score: 53.64% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x