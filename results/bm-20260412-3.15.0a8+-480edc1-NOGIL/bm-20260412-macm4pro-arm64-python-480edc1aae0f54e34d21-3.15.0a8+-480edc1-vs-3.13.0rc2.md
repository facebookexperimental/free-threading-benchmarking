# Results vs. 3.13.0rc2

- fork: python
- ref: 480edc1aae0f54e34d21
- machine: darwin-arm64
- commit hash: 480edc1
- commit date: 2026-04-12
- overall geometric mean: 1.011x faster
- HPT reliability: 55.32%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                     |
| docutils       | 1.05 sec                                                       | 995 ms: 1.05x faster                                                     |
| sphinx         | 409 ms                                                         | 422 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 241 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.61x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 118 ms: 1.21x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 189 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.6 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.6 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.0 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.27 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.1 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.1 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.5 ms: 1.23x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.86 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 894 ms: 1.12x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 57.3 ms: 1.09x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.14x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.82 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.13 ms: 1.20x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.6 ms: 1.06x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 12.0 ms: 1.20x slower                                                    |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| mako            | 4.41 ms                                                        | 5.60 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 809 us: 2.52x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 241 ms: 2.16x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 514 us: 1.93x faster                                                     |
| mdp                              | 1.06 sec                                                       | 606 ms: 1.74x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.61x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.15 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 999 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.1 us: 1.26x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.5 ms: 1.23x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 118 ms: 1.21x faster                                                     |
| go                               | 72.6 ms                                                        | 60.2 ms: 1.21x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.86 ms: 1.20x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.19x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 800 ns: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.27 ms: 1.15x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.7 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 194 ms: 1.15x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 894 ms: 1.12x faster                                                     |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 57.3 ms: 1.09x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 995 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| async_generators                 | 193 ms                                                         | 189 ms: 1.02x faster                                                     |
| pycparser                        | 470 ms                                                         | 460 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.05 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.1 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 422 ms: 1.03x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 334 ms: 1.04x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 685 ms: 1.05x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.3 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.6 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.1 ms: 1.07x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.07x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.62 us: 1.07x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.6 ns: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.12 ms: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.6 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.6 ms: 1.10x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.1 ms: 1.10x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                     |
| shortest_path                    | 225 ms                                                         | 250 ms: 1.11x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.19 ms: 1.12x slower                                                    |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 72.7 us: 1.12x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.6 ms: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.4 ms: 1.13x slower                                                    |
| thrift                           | 309 us                                                         | 350 us: 1.13x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.14x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.82 ms: 1.14x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.0 ms: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.8 ms: 1.16x slower                                                    |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 61.2 ms: 1.17x slower                                                    |
| connected_components             | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.13 ms: 1.20x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.15 us: 1.20x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 12.0 ms: 1.20x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.6 ms: 1.24x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.60 ms: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 48.3 ms: 1.28x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.28 ms: 1.28x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 55.4 ms: 1.30x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 44.5 ms: 1.32x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.0 ms: 1.34x slower                                                    |
| many_optionals                   | 200 us                                                         | 270 us: 1.35x slower                                                     |
| generators                       | 15.7 ms                                                        | 21.3 ms: 1.36x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 566 us: 1.37x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.6 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260412-3.15.0a8+-480edc1-NOGIL/bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 55.32% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.32x