# Results vs. 3.13.0rc2

- fork: python
- ref: 79321fdce3227cf09bb8
- machine: darwin-arm64
- commit hash: 79321fd
- commit date: 2026-04-22
- overall geometric mean: 1.032x faster
- HPT reliability: 70.09%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| docutils       | 1.05 sec                                                       | 988 ms: 1.06x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| sphinx         | 409 ms                                                         | 416 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 240 ms: 2.17x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 244 ms: 1.58x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.06x faster                                                     |
| async_generators                 | 193 ms                                                         | 185 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.8 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.1 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.1 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.10 ms: 1.18x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 94.0 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.6 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.7 ms: 1.22x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 845 ms: 1.18x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 57.7 ms: 1.08x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.50 ms: 1.10x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.63 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.8 ms: 1.07x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.0 ms: 1.10x slower                                                    |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| mako            | 4.41 ms                                                        | 5.69 ms: 1.29x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 810 us: 2.52x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 240 ms: 2.17x faster                                                     |
| pylint                           | 106 ms                                                         | 50.8 ms: 2.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 512 us: 1.94x faster                                                     |
| mdp                              | 1.06 sec                                                       | 603 ms: 1.75x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 244 ms: 1.58x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.12 ms: 1.52x faster                                                    |
| k_core                           | 1.46 sec                                                       | 987 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 106 us: 1.37x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.31x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| go                               | 72.6 ms                                                        | 58.6 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.7 ms: 1.22x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 798 ns: 1.19x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 845 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.10 ms: 1.18x faster                                                    |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.4 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                    |
| float                            | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 57.7 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                    |
| docutils                         | 1.05 sec                                                       | 988 ms: 1.06x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.06x faster                                                     |
| async_generators                 | 193 ms                                                         | 185 ms: 1.04x faster                                                     |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                     |
| pycparser                        | 470 ms                                                         | 455 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 94.0 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 416 ms: 1.02x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 332 ms: 1.03x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.04x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 675 ms: 1.04x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.33 us: 1.04x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.57 us: 1.05x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.2 ms: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.6 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.06x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.04 ms: 1.07x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.8 ms: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.6 ms: 1.08x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.09x slower                                                     |
| thrift                           | 309 us                                                         | 339 us: 1.10x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 44.6 ns: 1.10x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.50 ms: 1.10x slower                                                    |
| shortest_path                    | 225 ms                                                         | 247 ms: 1.10x slower                                                     |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.0 ms: 1.10x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.1 ms: 1.10x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.4 us: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.8 ms: 1.11x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.2 ms: 1.11x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.63 ms: 1.11x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.1 ms: 1.12x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.13x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 50.0 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.9 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.6 ms: 1.16x slower                                                    |
| connected_components             | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| raytrace                         | 109 ms                                                         | 127 ms: 1.16x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 186 ms: 1.17x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.12 us: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.22 ms: 1.25x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.5 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 54.3 ms: 1.27x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.1 ms: 1.28x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.69 ms: 1.29x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 44.0 ms: 1.31x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.9 ms: 1.33x slower                                                    |
| many_optionals                   | 200 us                                                         | 268 us: 1.34x slower                                                     |
| nbody                            | 42.5 ms                                                        | 57.1 ms: 1.34x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 570 us: 1.38x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.1 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (2): telco, json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260422-3.15.0a8+-79321fd-NOGIL/bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.032x faster

# HPT report

- Reliability score: 70.09% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.32x