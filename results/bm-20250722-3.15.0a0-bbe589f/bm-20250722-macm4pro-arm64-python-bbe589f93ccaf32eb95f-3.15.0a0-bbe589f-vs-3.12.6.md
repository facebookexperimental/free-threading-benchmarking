# Results vs. 3.12.6

- fork: python
- ref: bbe589f93ccaf32eb95f
- machine: darwin-arm64
- commit hash: bbe589f
- commit date: 2025-07-22
- overall geometric mean: 1.092x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 416 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 246 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.7 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.9 ms: 2.74x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.6 ms: 1.24x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.7 ms: 1.11x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.7 ms: 1.12x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.8 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.9 ms: 1.15x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 62.3 ms: 1.09x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.02x faster                                                    |
| tomli_loads          | 957 ms                                                   | 941 ms: 1.02x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.02x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.49 ms: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.78 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.28 ms: 1.10x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.98 ms: 1.05x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.7 ms: 1.01x faster                                                   |
| mako            | 4.77 ms                                                  | 4.85 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 246 ms: 2.01x faster                                                    |
| mdp                              | 1.09 sec                                                 | 545 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                   |
| deepcopy                         | 161 us                                                   | 112 us: 1.44x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.54 us: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.3 ns: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                   |
| float                            | 37.9 ms                                                  | 30.6 ms: 1.24x faster                                                   |
| go                               | 70.0 ms                                                  | 56.5 ms: 1.24x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 44.5 ms: 1.22x faster                                                   |
| raytrace                         | 145 ms                                                   | 119 ms: 1.22x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.0 ms: 1.22x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.7 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.4 ms: 1.19x faster                                                   |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| k_core                           | 1.12 sec                                                 | 958 ms: 1.17x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.9 ms: 1.15x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.52 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.6 ms: 1.13x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.7 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| typing_runtime_protocols         | 71.0 us                                                  | 63.8 us: 1.11x faster                                                   |
| nbody                            | 54.2 ms                                                  | 48.7 ms: 1.11x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                   |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.4 ms: 1.09x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.7 ms: 1.09x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 62.3 ms: 1.09x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.3 ms: 1.09x faster                                                   |
| pyflate                          | 216 ms                                                   | 199 ms: 1.09x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.58 us: 1.09x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.37 us: 1.08x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.82 ms: 1.08x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.93 ms: 1.07x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.1 ms: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.54 ms: 1.06x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.1 ms: 1.05x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 135 ms: 1.05x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.3 ms: 1.05x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.98 ms: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 309 us: 1.04x faster                                                    |
| sphinx                           | 434 ms                                                   | 416 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 49.8 ms: 1.03x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.02x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.0 ms: 1.02x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 97.8 ms: 1.02x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 941 ms: 1.02x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 323 ms: 1.01x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 657 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 956 ns: 1.01x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 57.1 ms: 1.01x faster                                                   |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.7 ms: 1.01x faster                                                   |
| connected_components             | 201 ms                                                   | 201 ms: 1.00x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.85 ms: 1.02x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.02x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 436 us: 1.04x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                    |
| fannkuch                         | 176 ms                                                   | 184 ms: 1.05x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.10 ms: 1.05x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.49 ms: 1.05x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 50.8 ms: 1.06x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.78 ms: 1.10x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.28 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.2 ms: 1.11x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 956 us: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.09 ms: 1.18x slower                                                   |
| coverage                         | 26.9 ms                                                  | 32.6 ms: 1.21x slower                                                   |
| many_optionals                   | 195 us                                                   | 321 us: 1.65x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.9 ms: 2.74x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (2): json, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250722-3.15.0a0-bbe589f/bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.092x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x