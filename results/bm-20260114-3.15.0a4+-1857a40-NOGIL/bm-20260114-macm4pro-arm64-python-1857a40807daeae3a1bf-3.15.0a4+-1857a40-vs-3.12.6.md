# Results vs. 3.12.6

- fork: python
- ref: 1857a40807daeae3a1bf
- machine: darwin-arm64
- commit hash: 1857a40
- commit date: 2026-01-14
- overall geometric mean: 1.082x faster
- HPT reliability: 97.41%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.09x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| sphinx         | 434 ms                                                   | 430 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 246 ms: 1.81x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.59x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.53x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 272 ms: 1.23x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                     |
| async_generators                 | 206 ms                                                   | 190 ms: 1.08x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.1 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 95.0 ms: 2.96x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                    |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.3 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.5 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.31 ms: 1.03x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.1 ms: 1.35x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.9 ms: 1.19x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.01 ms: 1.06x faster                                                    |
| tomli_loads          | 957 ms                                                   | 904 ms: 1.06x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 37.6 ms: 1.03x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.1 ms: 1.02x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.97 ms: 1.24x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.23 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.26x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                    |
| django_template | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| mako            | 4.77 ms                                                  | 5.56 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.18 ms: 4.97x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 825 us: 2.44x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 246 ms: 1.81x faster                                                     |
| mdp                              | 1.09 sec                                                 | 604 ms: 1.81x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 521 us: 1.59x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.59x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.53x faster                                                     |
| deepcopy                         | 161 us                                                   | 109 us: 1.49x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.43x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.1 ms: 1.35x faster                                                    |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.19 us: 1.23x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 272 ms: 1.23x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 56.9 ms: 1.19x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.37 us: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 827 ns: 1.17x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 43.8 ns: 1.16x faster                                                    |
| go                               | 70.0 ms                                                  | 60.6 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                     |
| raytrace                         | 145 ms                                                   | 128 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 996 ms: 1.12x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.7 ms: 1.11x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                     |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                     |
| async_generators                 | 206 ms                                                   | 190 ms: 1.08x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 50.4 ms: 1.08x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.01 ms: 1.06x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.5 ms: 1.06x faster                                                    |
| pylint                           | 128 ms                                                   | 121 ms: 1.06x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 904 ms: 1.06x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.44 us: 1.06x faster                                                    |
| pycparser                        | 497 ms                                                   | 475 ms: 1.05x faster                                                     |
| generators                       | 21.9 ms                                                  | 21.1 ms: 1.04x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.70 us: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.6 ms: 1.03x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.31 ms: 1.03x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.3 ms: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 43.1 ms: 1.01x faster                                                    |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                     |
| sphinx                           | 434 ms                                                   | 430 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 71.5 us: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.1 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 333 ms: 1.02x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.11 ms: 1.02x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.21 ms: 1.02x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.0 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 686 ms: 1.03x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.1 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.17 ms: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.5 ms: 1.05x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 26.8 ms: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.3 ms: 1.06x slower                                                    |
| thrift                           | 322 us                                                   | 341 us: 1.06x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 61.1 ms: 1.06x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.0 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                    |
| 2to3                             | 114 ms                                                   | 124 ms: 1.09x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 191 ms: 1.14x slower                                                     |
| shortest_path                    | 219 ms                                                   | 252 ms: 1.15x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.04 ms: 1.16x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.56 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 47.2 ms: 1.19x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.9 ms: 1.19x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 61.3 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 246 ms: 1.23x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.97 ms: 1.24x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.23 ms: 1.27x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 549 us: 1.31x slower                                                     |
| many_optionals                   | 195 us                                                   | 277 us: 1.42x slower                                                     |
| coverage                         | 26.9 ms                                                  | 39.1 ms: 1.46x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 95.0 ms: 2.96x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260114-3.15.0a4+-1857a40-NOGIL/bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 97.41% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.35x