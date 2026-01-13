# Results vs. 3.12.6

- fork: python
- ref: a6bc60da02ea37f33d5a
- machine: darwin-arm64
- commit hash: a6bc60d
- commit date: 2026-01-12
- overall geometric mean: 1.082x faster
- HPT reliability: 98.27%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| sphinx         | 434 ms                                                   | 430 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 253 ms: 1.90x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.57x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                     |
| async_generators                 | 206 ms                                                   | 189 ms: 1.09x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.7 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.8 ms: 2.95x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                    |
| nbody          | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                    |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.2 ms: 1.07x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.24 ms: 1.04x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.6 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.8 ms: 1.30x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.3 ms: 1.15x faster                                                    |
| tomli_loads          | 957 ms                                                   | 891 ms: 1.07x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.99 ms: 1.07x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.7 ms: 1.03x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 149 us: 1.07x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.0 ms: 1.25x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.26 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.26x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 24.2 ms: 1.11x slower                                                    |
| django_template | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                    |
| mako            | 4.77 ms                                                  | 5.60 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.17 ms: 4.98x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 810 us: 2.48x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 253 ms: 1.90x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                     |
| mdp                              | 1.09 sec                                                 | 610 ms: 1.79x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 513 us: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.57x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| deepcopy                         | 161 us                                                   | 109 us: 1.48x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                    |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.8 ms: 1.30x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.19 us: 1.23x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.35 us: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 829 ns: 1.17x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 43.9 ns: 1.16x faster                                                    |
| go                               | 70.0 ms                                                  | 60.8 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 59.3 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.13x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                   |
| raytrace                         | 145 ms                                                   | 129 ms: 1.12x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.6 ms: 1.12x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 196 ms: 1.11x faster                                                     |
| async_generators                 | 206 ms                                                   | 189 ms: 1.09x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 50.1 ms: 1.09x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 891 ms: 1.07x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.99 ms: 1.07x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.2 ms: 1.07x faster                                                    |
| pylint                           | 128 ms                                                   | 121 ms: 1.06x faster                                                     |
| pycparser                        | 497 ms                                                   | 474 ms: 1.05x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.45 us: 1.05x faster                                                    |
| generators                       | 21.9 ms                                                  | 21.1 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.24 ms: 1.04x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.71 us: 1.03x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.7 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.6 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.68 ms: 1.03x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.2 ms: 1.03x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 42.9 ms: 1.01x faster                                                    |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                     |
| sphinx                           | 434 ms                                                   | 430 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.10 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 71.9 us: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 333 ms: 1.02x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.8 ms: 1.02x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.25 ms: 1.03x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 685 ms: 1.03x slower                                                     |
| richards                         | 22.4 ms                                                  | 23.4 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                    |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.7 ms: 1.05x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.18 ms: 1.05x slower                                                    |
| thrift                           | 322 us                                                   | 339 us: 1.05x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 149 us: 1.07x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 61.5 ms: 1.07x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.2 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                     |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.08x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 41.8 ms: 1.08x slower                                                    |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 24.2 ms: 1.11x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 58.3 ms: 1.14x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 191 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                     |
| shortest_path                    | 219 ms                                                   | 255 ms: 1.16x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.60 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.4 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.9 ms: 1.18x slower                                                    |
| connected_components             | 201 ms                                                   | 248 ms: 1.23x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 10.0 ms: 1.25x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.26 ms: 1.27x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 551 us: 1.32x slower                                                     |
| many_optionals                   | 195 us                                                   | 271 us: 1.39x slower                                                     |
| coverage                         | 26.9 ms                                                  | 39.2 ms: 1.46x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.8 ms: 2.95x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260112-3.15.0a3+-a6bc60d-NOGIL/bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 98.27% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.35x