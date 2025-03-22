# Results vs. 3.13.0rc2

- fork: python
- ref: 49fb75c676bd422b03ae
- machine: darwin-arm64
- commit hash: 49fb75c
- commit date: 2025-03-21
- overall geometric mean: 1.003x slower
- HPT reliability: 77.13%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.00x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                   |
| html5lib       | 23.1 ms                                                        | 23.0 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 417 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 261 ms: 2.02x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 263 ms: 1.98x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 261 ms: 1.55x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 263 ms: 1.47x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 151 ms: 1.23x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.22x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 134 ms: 1.31x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 90.4 ms: 3.12x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| float          | 31.4 ms                                                        | 32.9 ms: 1.05x slower                                                    |
| nbody          | 42.5 ms                                                        | 51.1 ms: 1.20x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.4 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 859 ms: 1.16x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.4 ms: 1.04x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.6 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 105 us: 1.05x slower                                                     |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.10 ms: 1.10x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.46 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                                    |
| mako            | 4.41 ms                                                        | 4.89 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 15.8 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 261 ms: 2.02x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 263 ms: 1.98x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 261 ms: 1.55x faster                                                     |
| k_core                           | 1.46 sec                                                       | 965 ms: 1.52x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 263 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.9 us: 1.28x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| go                               | 72.6 ms                                                        | 58.7 ms: 1.24x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 151 ms: 1.23x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.22x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.20x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.7 ms: 1.17x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 859 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.6 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 913 us: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| pyflate                          | 222 ms                                                         | 207 ms: 1.07x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.4 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.6 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| connected_components             | 208 ms                                                         | 204 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.10 sec: 1.01x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 93.4 ms: 1.01x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.8 ms: 1.01x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 23.0 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 24.6 ms: 1.00x faster                                                    |
| 2to3                             | 112 ms                                                         | 112 ms: 1.00x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 38.0 ms: 1.01x slower                                                    |
| thrift                           | 309 us                                                         | 311 us: 1.01x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 44.9 ms: 1.01x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.02x slower                                                    |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 662 ms: 1.02x slower                                                     |
| sphinx                           | 409 ms                                                         | 417 ms: 1.02x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 329 ms: 1.02x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.14 ms: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.2 ms: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.12 ms: 1.04x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.6 ms: 1.04x slower                                                    |
| mdp                              | 1.06 sec                                                       | 1.10 sec: 1.04x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 67.6 us: 1.05x slower                                                    |
| float                            | 31.4 ms                                                        | 32.9 ms: 1.05x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.24 ms: 1.05x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.2 ms: 1.05x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 105 us: 1.05x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 433 us: 1.05x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.92 ms: 1.05x slower                                                    |
| pycparser                        | 470 ms                                                         | 496 ms: 1.05x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.00 ms: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.89 ms: 1.06x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 31.9 ms: 1.07x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.39 us: 1.07x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                     |
| fannkuch                         | 179 ms                                                         | 192 ms: 1.07x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 171 ms: 1.07x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.5 ms: 1.08x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 134 ms: 1.08x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.46 ms: 1.09x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.58 ms: 1.09x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.10 ms: 1.10x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.7 ns: 1.10x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.89 ms: 1.11x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 49.8 ms: 1.14x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 48.9 ms: 1.14x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.79 us: 1.15x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.0 ms: 1.16x slower                                                    |
| raytrace                         | 109 ms                                                         | 126 ms: 1.16x slower                                                     |
| many_optionals                   | 200 us                                                         | 235 us: 1.17x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 43.8 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.7 ms: 1.19x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 40.3 ms: 1.20x slower                                                    |
| nbody                            | 42.5 ms                                                        | 51.1 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.8 ms: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 134 ms: 1.31x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.71 ms: 1.39x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 90.4 ms: 3.12x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (2): async_tree_eager, sqlite_synth
Ignored benchmarks (8) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250321-3.14.0a6+-49fb75c/bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 77.13% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.07x