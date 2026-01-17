# Results vs. 3.12.6

- fork: python
- ref: 3199cfcf7661b0c9bd73
- machine: darwin-arm64
- commit hash: 3199cfc
- commit date: 2026-01-16
- overall geometric mean: 1.139x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.00x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 22.0 ms: 1.04x faster                                                    |
| sphinx         | 434 ms                                                   | 400 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 226 ms: 2.20x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 228 ms: 2.10x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 224 ms: 1.99x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 239 ms: 1.93x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 105 ms: 1.70x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 102 ms: 1.69x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 141 ms: 1.57x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.7 ms: 1.09x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.4 ms: 2.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.31x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.0 ms: 1.36x faster                                                    |
| nbody          | 54.2 ms                                                  | 46.1 ms: 1.18x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.16x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.0 ms: 1.16x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.1 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.77 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.3 ms: 1.31x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.83 ms: 1.11x faster                                                    |
| tomli_loads          | 957 ms                                                   | 863 ms: 1.11x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 61.4 ms: 1.11x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 99.5 us: 1.03x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.03x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.81 ms: 1.10x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.34 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.98 ms: 1.05x faster                                                    |
| mako            | 4.77 ms                                                  | 4.84 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.10 ms: 5.07x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 226 ms: 2.20x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 228 ms: 2.10x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 224 ms: 1.99x faster                                                     |
| mdp                              | 1.09 sec                                                 | 554 ms: 1.97x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 239 ms: 1.93x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 105 ms: 1.70x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 102 ms: 1.69x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| deepcopy                         | 161 us                                                   | 101 us: 1.61x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.6 us: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 141 ms: 1.57x faster                                                     |
| float                            | 37.9 ms                                                  | 28.0 ms: 1.36x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.32 us: 1.34x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.10 us: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.3 ms: 1.31x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.27x faster                                                    |
| go                               | 70.0 ms                                                  | 56.2 ms: 1.25x faster                                                    |
| raytrace                         | 145 ms                                                   | 117 ms: 1.24x faster                                                     |
| k_core                           | 1.12 sec                                                 | 906 ms: 1.23x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 50.1 ms: 1.22x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.0 ms: 1.21x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.2 ns: 1.18x faster                                                    |
| nbody                            | 54.2 ms                                                  | 46.1 ms: 1.18x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 121 ms: 1.17x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 47.0 ms: 1.16x faster                                                    |
| pyflate                          | 216 ms                                                   | 187 ms: 1.15x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.83 ms: 1.14x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.6 ms: 1.13x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.53 ms: 1.13x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.6 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.29 us: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.51 us: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.01 sec: 1.12x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.83 ms: 1.11x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 863 ms: 1.11x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 61.4 ms: 1.11x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.4 us: 1.10x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 46.7 ms: 1.10x faster                                                    |
| pylint                           | 128 ms                                                   | 117 ms: 1.10x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 39.6 ms: 1.10x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.7 ms: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 400 ms: 1.08x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 23.5 ms: 1.08x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.8 ms: 1.08x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.4 ms: 1.07x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.85 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.61 ms: 1.05x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                    |
| pycparser                        | 497 ms                                                   | 474 ms: 1.05x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 9.98 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.0 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.1 ms: 1.04x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 99.5 us: 1.03x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 320 ms: 1.03x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 650 ms: 1.02x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 56.5 ms: 1.02x faster                                                    |
| thrift                           | 322 us                                                   | 316 us: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| sympy_str                        | 104 ms                                                   | 103 ms: 1.01x faster                                                     |
| fannkuch                         | 176 ms                                                   | 173 ms: 1.01x faster                                                     |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.00x slower                                                     |
| sqlite_synth                     | 967 ns                                                   | 977 ns: 1.01x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.84 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.77 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.03x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.04x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 174 ms: 1.04x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 437 us: 1.04x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.0 ms: 1.05x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.07x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.86 ms: 1.10x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.81 ms: 1.10x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.34 ms: 1.11x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 924 us: 1.11x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.13x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.3 ms: 1.14x slower                                                    |
| connected_components             | 201 ms                                                   | 235 ms: 1.17x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.3 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 257 us: 1.32x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.4 ms: 2.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                             |

Benchmark hidden because not significant (1): genshi_xml
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260116-3.15.0a5+-3199cfc/bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.139x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.22x