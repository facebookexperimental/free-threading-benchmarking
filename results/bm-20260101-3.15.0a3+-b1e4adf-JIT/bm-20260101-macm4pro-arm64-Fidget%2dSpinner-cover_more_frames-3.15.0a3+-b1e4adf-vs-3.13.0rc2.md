# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: cover_more_frames
- machine: darwin-arm64
- commit hash: b1e4adf
- commit date: 2026-01-01
- overall geometric mean: 1.149x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.00x slower                                                            |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                          |
| html5lib       | 23.1 ms                                                        | 20.2 ms: 1.14x faster                                                           |
| sphinx         | 409 ms                                                         | 391 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                          | 1.05x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.36x faster                                                            |
| async_tree_eager_io              | 525 ms                                                         | 223 ms: 2.35x faster                                                            |
| async_tree_io_tg                 | 405 ms                                                         | 222 ms: 1.82x faster                                                            |
| async_tree_io                    | 386 ms                                                         | 232 ms: 1.67x faster                                                            |
| async_tree_none                  | 142 ms                                                         | 99.7 ms: 1.43x faster                                                           |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                            |
| async_tree_none_tg               | 133 ms                                                         | 98.6 ms: 1.35x faster                                                           |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.34x faster                                                            |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                            |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                            |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                            |
| async_tree_eager                 | 43.2 ms                                                        | 38.1 ms: 1.13x faster                                                           |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                           |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                            |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                            |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.02x faster                                                            |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                            |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                            |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.5 ms: 2.75x slower                                                           |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 23.0 ms: 1.37x faster                                                           |
| nbody          | 42.5 ms                                                        | 39.8 ms: 1.07x faster                                                           |
| pidigits       | 166 ms                                                         | 164 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                          | 1.14x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 40.1 ms: 1.20x faster                                                           |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                           |
| regex_v8       | 10.7 ms                                                        | 9.74 ms: 1.10x faster                                                           |
| regex_dna      | 94.6 ms                                                        | 95.4 ms: 1.01x slower                                                           |
| Geometric mean | (ref)                                                          | 1.10x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 99.5 us                                                        | 73.1 us: 1.36x faster                                                           |
| json_dumps           | 4.65 ms                                                        | 3.68 ms: 1.26x faster                                                           |
| tomli_loads          | 1000 ms                                                        | 809 ms: 1.24x faster                                                            |
| xml_etree_iterparse  | 46.1 ms                                                        | 37.5 ms: 1.23x faster                                                           |
| xml_etree_generate   | 35.8 ms                                                        | 30.7 ms: 1.17x faster                                                           |
| xml_etree_process    | 25.4 ms                                                        | 21.9 ms: 1.16x faster                                                           |
| pickle_pure_python   | 130 us                                                         | 113 us: 1.15x faster                                                            |
| xml_etree_parse      | 62.4 ms                                                        | 60.3 ms: 1.03x faster                                                           |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                           |
| Geometric mean       | (ref)                                                          | 1.17x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|------------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                           |
| python_startup_no_site | 5.95 ms                                                        | 6.38 ms: 1.07x slower                                                           |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|-----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 3.91 ms: 1.13x faster                                                           |
| genshi_text     | 9.97 ms                                                        | 8.89 ms: 1.12x faster                                                           |
| genshi_xml      | 21.4 ms                                                        | 20.5 ms: 1.04x faster                                                           |
| django_template | 12.5 ms                                                        | 13.9 ms: 1.11x slower                                                           |
| Geometric mean  | (ref)                                                          | 1.04x faster                                                                    |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.36x faster                                                            |
| async_tree_eager_io              | 525 ms                                                         | 223 ms: 2.35x faster                                                            |
| richards                         | 22.1 ms                                                        | 9.77 ms: 2.26x faster                                                           |
| richards_super                   | 24.7 ms                                                        | 11.6 ms: 2.12x faster                                                           |
| async_tree_io_tg                 | 405 ms                                                         | 222 ms: 1.82x faster                                                            |
| mdp                              | 1.06 sec                                                       | 585 ms: 1.81x faster                                                            |
| k_core                           | 1.46 sec                                                       | 867 ms: 1.69x faster                                                            |
| go                               | 72.6 ms                                                        | 43.2 ms: 1.68x faster                                                           |
| async_tree_io                    | 386 ms                                                         | 232 ms: 1.67x faster                                                            |
| subparsers                       | 6.26 ms                                                        | 3.92 ms: 1.60x faster                                                           |
| pyflate                          | 222 ms                                                         | 145 ms: 1.53x faster                                                            |
| scimark_sor                      | 64.0 ms                                                        | 42.1 ms: 1.52x faster                                                           |
| deepcopy                         | 145 us                                                         | 97.8 us: 1.48x faster                                                           |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.43x faster                                                           |
| async_tree_none                  | 142 ms                                                         | 99.7 ms: 1.43x faster                                                           |
| float                            | 31.4 ms                                                        | 23.0 ms: 1.37x faster                                                           |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                            |
| unpickle_pure_python             | 99.5 us                                                        | 73.1 us: 1.36x faster                                                           |
| async_tree_none_tg               | 133 ms                                                         | 98.6 ms: 1.35x faster                                                           |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.34x faster                                                            |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.5 ms: 1.33x faster                                                           |
| deltablue                        | 1.45 ms                                                        | 1.12 ms: 1.29x faster                                                           |
| deepcopy_reduce                  | 1.30 us                                                        | 1.00 us: 1.29x faster                                                           |
| json_dumps                       | 4.65 ms                                                        | 3.68 ms: 1.26x faster                                                           |
| pprint_safe_repr                 | 322 ms                                                         | 259 ms: 1.24x faster                                                            |
| pprint_pformat                   | 650 ms                                                         | 524 ms: 1.24x faster                                                            |
| tomli_loads                      | 1000 ms                                                        | 809 ms: 1.24x faster                                                            |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.5 ms: 1.23x faster                                                           |
| scimark_fft                      | 124 ms                                                         | 101 ms: 1.23x faster                                                            |
| telco                            | 3.07 ms                                                        | 2.52 ms: 1.22x faster                                                           |
| logging_silent                   | 40.6 ns                                                        | 33.7 ns: 1.20x faster                                                           |
| regex_compile                    | 47.9 ms                                                        | 40.1 ms: 1.20x faster                                                           |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                            |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                            |
| scimark_lu                       | 42.8 ms                                                        | 36.5 ms: 1.17x faster                                                           |
| fannkuch                         | 179 ms                                                         | 153 ms: 1.17x faster                                                            |
| xml_etree_generate               | 35.8 ms                                                        | 30.7 ms: 1.17x faster                                                           |
| xml_etree_process                | 25.4 ms                                                        | 21.9 ms: 1.16x faster                                                           |
| pickle_pure_python               | 130 us                                                         | 113 us: 1.15x faster                                                            |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.85 sec: 1.15x faster                                                          |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                            |
| html5lib                         | 23.1 ms                                                        | 20.2 ms: 1.14x faster                                                           |
| async_tree_eager                 | 43.2 ms                                                        | 38.1 ms: 1.13x faster                                                           |
| mako                             | 4.41 ms                                                        | 3.91 ms: 1.13x faster                                                           |
| genshi_text                      | 9.97 ms                                                        | 8.89 ms: 1.12x faster                                                           |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                           |
| comprehensions                   | 6.80 us                                                        | 6.16 us: 1.10x faster                                                           |
| chaos                            | 24.3 ms                                                        | 22.0 ms: 1.10x faster                                                           |
| regex_v8                         | 10.7 ms                                                        | 9.74 ms: 1.10x faster                                                           |
| hexiom                           | 2.85 ms                                                        | 2.63 ms: 1.08x faster                                                           |
| crypto_pyaes                     | 33.6 ms                                                        | 31.1 ms: 1.08x faster                                                           |
| spectral_norm                    | 43.7 ms                                                        | 40.8 ms: 1.07x faster                                                           |
| pycparser                        | 470 ms                                                         | 440 ms: 1.07x faster                                                            |
| thrift                           | 309 us                                                         | 289 us: 1.07x faster                                                            |
| nbody                            | 42.5 ms                                                        | 39.8 ms: 1.07x faster                                                           |
| create_gc_cycles                 | 993 us                                                         | 933 us: 1.06x faster                                                            |
| logging_simple                   | 2.24 us                                                        | 2.11 us: 1.06x faster                                                           |
| logging_format                   | 2.45 us                                                        | 2.32 us: 1.05x faster                                                           |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                           |
| meteor_contest                   | 47.9 ms                                                        | 45.6 ms: 1.05x faster                                                           |
| connected_components             | 208 ms                                                         | 198 ms: 1.05x faster                                                            |
| genshi_xml                       | 21.4 ms                                                        | 20.5 ms: 1.04x faster                                                           |
| sphinx                           | 409 ms                                                         | 391 ms: 1.04x faster                                                            |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                            |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.04x faster                                                            |
| typing_runtime_protocols         | 64.6 us                                                        | 62.3 us: 1.04x faster                                                           |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.04x faster                                                           |
| dulwich_log                      | 19.8 ms                                                        | 19.2 ms: 1.04x faster                                                           |
| xml_etree_parse                  | 62.4 ms                                                        | 60.3 ms: 1.03x faster                                                           |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                            |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                          |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.02x faster                                                            |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                           |
| raytrace                         | 109 ms                                                         | 107 ms: 1.02x faster                                                            |
| pidigits                         | 166 ms                                                         | 164 ms: 1.02x faster                                                            |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                           |
| 2to3                             | 112 ms                                                         | 112 ms: 1.00x slower                                                            |
| regex_dna                        | 94.6 ms                                                        | 95.4 ms: 1.01x slower                                                           |
| sympy_integrate                  | 7.53 ms                                                        | 7.60 ms: 1.01x slower                                                           |
| sqlite_synth                     | 948 ns                                                         | 964 ns: 1.02x slower                                                            |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                           |
| python_startup                   | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                           |
| nqueens                          | 37.2 ms                                                        | 38.4 ms: 1.03x slower                                                           |
| bench_thread_pool                | 412 us                                                         | 426 us: 1.03x slower                                                            |
| python_startup_no_site           | 5.95 ms                                                        | 6.38 ms: 1.07x slower                                                           |
| coverage                         | 31.2 ms                                                        | 33.8 ms: 1.08x slower                                                           |
| sympy_sum                        | 52.3 ms                                                        | 56.6 ms: 1.08x slower                                                           |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.93 ms: 1.09x slower                                                           |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                            |
| sympy_str                        | 95.5 ms                                                        | 106 ms: 1.11x slower                                                            |
| django_template                  | 12.5 ms                                                        | 13.9 ms: 1.11x slower                                                           |
| pylint                           | 106 ms                                                         | 123 ms: 1.17x slower                                                            |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                            |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                            |
| bench_mp_pool                    | 37.8 ms                                                        | 45.6 ms: 1.21x slower                                                           |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                           |
| many_optionals                   | 200 us                                                         | 256 us: 1.28x slower                                                            |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.5 ms: 2.75x slower                                                           |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                                    |
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260101-3.15.0a3+-b1e4adf-JIT/bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.149x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.20x