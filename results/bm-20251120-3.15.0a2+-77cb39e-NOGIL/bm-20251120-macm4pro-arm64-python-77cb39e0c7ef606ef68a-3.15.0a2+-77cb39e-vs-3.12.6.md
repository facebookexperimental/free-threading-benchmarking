# Results vs. 3.12.6

- fork: python
- ref: 77cb39e0c7ef606ef68a
- machine: darwin-arm64
- commit hash: 77cb39e
- commit date: 2025-11-20
- overall geometric mean: 1.106x faster
- HPT reliability: 99.83%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.05x slower                                                     |
| docutils       | 1.02 sec                                                 | 995 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.9 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 417 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 200 ms: 2.48x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 191 ms: 2.34x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.3 ms: 2.02x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.88x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 98.7 ms: 1.81x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.73x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.3 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.8 ms: 2.39x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.39x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.4 ms: 1.38x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 54.9 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.5 ms: 1.06x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.0 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.36 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.2 ms: 1.19x faster                                                    |
| tomli_loads          | 957 ms                                                   | 874 ms: 1.10x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.95 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.75 ms: 1.22x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.08 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.1 ms: 1.06x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| mako            | 4.77 ms                                                  | 5.59 ms: 1.17x slower                                                    |
| django_template | 13.6 ms                                                  | 16.0 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 765 us: 2.62x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 200 ms: 2.48x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 191 ms: 2.34x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.3 ms: 2.02x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.88x faster                                                     |
| mdp                              | 1.09 sec                                                 | 595 ms: 1.84x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 98.7 ms: 1.81x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 475 us: 1.75x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.73x faster                                                     |
| deepcopy                         | 161 us                                                   | 109 us: 1.48x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                     |
| float                            | 37.9 ms                                                  | 27.4 ms: 1.38x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.06 us: 1.22x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.20 us: 1.22x faster                                                    |
| go                               | 70.0 ms                                                  | 58.8 ms: 1.19x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.2 ms: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 825 ns: 1.17x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 44.4 ns: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.3 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                   |
| raytrace                         | 145 ms                                                   | 128 ms: 1.14x faster                                                     |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                    |
| pyflate                          | 216 ms                                                   | 192 ms: 1.13x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.12x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 18.6 ms: 1.12x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.1 ms: 1.11x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 874 ms: 1.10x faster                                                     |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.95 ms: 1.08x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 464 ms: 1.07x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 51.3 ms: 1.06x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.5 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.45 us: 1.05x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.6 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 417 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 96.0 ms: 1.04x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.71 us: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 995 ms: 1.03x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.36 ms: 1.02x faster                                                    |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.9 ms: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.09 ms: 1.01x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.07 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 71.7 us: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody                            | 54.2 ms                                                  | 54.9 ms: 1.01x slower                                                    |
| richards                         | 22.4 ms                                                  | 22.9 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 334 ms: 1.02x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.1 ms: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.1 ms: 1.03x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 685 ms: 1.03x slower                                                     |
| thrift                           | 322 us                                                   | 332 us: 1.03x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.3 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.17 ms: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 119 ms: 1.05x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.05x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.6 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.1 ms: 1.06x slower                                                    |
| dask                             | 528 ms                                                   | 561 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.4 ms: 1.09x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.6 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.59 ms: 1.17x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.0 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.2 ms: 1.18x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.75 ms: 1.22x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.08 ms: 1.24x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 64.4 ms: 1.26x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 561 us: 1.34x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.0 ms: 1.49x slower                                                    |
| many_optionals                   | 195 us                                                   | 376 us: 1.93x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.8 ms: 2.39x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (1): nqueens
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251120-3.15.0a2+-77cb39e-NOGIL/bm-20251120-macm4pro-arm64-python-77cb39e0c7ef606ef68a-3.15.0a2+-77cb39e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.106x faster

# HPT report

- Reliability score: 99.83% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.36x