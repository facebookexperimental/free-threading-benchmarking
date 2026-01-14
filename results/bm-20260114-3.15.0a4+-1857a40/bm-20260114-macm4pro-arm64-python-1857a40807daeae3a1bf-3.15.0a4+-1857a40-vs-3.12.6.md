# Results vs. 3.12.6

- fork: python
- ref: 1857a40807daeae3a1bf
- machine: darwin-arm64
- commit hash: 1857a40
- commit date: 2026-01-14
- overall geometric mean: 1.158x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.00x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 21.7 ms: 1.06x faster                                                    |
| sphinx         | 434 ms                                                   | 398 ms: 1.09x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 227 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 237 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.71x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 249 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.5 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 237 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.9 ms: 2.49x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.32x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.6 ms: 1.22x faster                                                    |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                    | 1.17x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.1 ms: 1.21x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.0 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.3 ms: 1.35x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.4 ms: 1.13x faster                                                    |
| tomli_loads          | 957 ms                                                   | 849 ms: 1.13x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 60.6 ms: 1.12x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 95.8 us: 1.07x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 142 us: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.03 ms: 1.13x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.50 ms: 1.14x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.13x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.74 ms: 1.08x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| mako            | 4.77 ms                                                  | 4.70 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 14.9 ms: 1.10x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.09 ms: 5.08x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 227 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.01x faster                                                     |
| mdp                              | 1.09 sec                                                 | 543 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 237 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.71x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| deepcopy                         | 161 us                                                   | 99.7 us: 1.62x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.4 us: 1.60x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| float                            | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.13 us: 1.38x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.08 us: 1.35x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.3 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 249 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| go                               | 70.0 ms                                                  | 52.9 ms: 1.32x faster                                                    |
| raytrace                         | 145 ms                                                   | 115 ms: 1.27x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.7 ms: 1.24x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.9 ns: 1.24x faster                                                    |
| k_core                           | 1.12 sec                                                 | 901 ms: 1.24x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.6 ms: 1.23x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.6 ms: 1.22x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 45.1 ms: 1.21x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 119 ms: 1.19x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.5 ms: 1.19x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.77 ms: 1.17x faster                                                    |
| pyflate                          | 216 ms                                                   | 185 ms: 1.17x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.48 ms: 1.17x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.7 ms: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| chaos                            | 28.9 ms                                                  | 25.1 ms: 1.15x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.44 us: 1.15x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 44.8 ms: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.3 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.8 us: 1.13x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.4 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 849 ms: 1.13x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.5 ms: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.6 ms: 1.12x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.8 ms: 1.11x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.2 ms: 1.11x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.76 ms: 1.10x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                     |
| sphinx                           | 434 ms                                                   | 398 ms: 1.09x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.74 ms: 1.08x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 95.8 us: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 466 ms: 1.07x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.53 ms: 1.07x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 624 ms: 1.07x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.7 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 310 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| thrift                           | 322 us                                                   | 309 us: 1.04x faster                                                     |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.8 ms: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 97.0 ms: 1.03x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.70 ms: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                    |
| 2to3                             | 114 ms                                                   | 113 ms: 1.00x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                     |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 142 us: 1.02x slower                                                     |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                     |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.10 ms: 1.05x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 50.7 ms: 1.06x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.85 ms: 1.09x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.9 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 237 ms: 1.12x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.03 ms: 1.13x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.50 ms: 1.14x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 949 us: 1.14x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.8 ms: 1.15x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.2 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 255 us: 1.31x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.9 ms: 2.49x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                             |

Benchmark hidden because not significant (2): json_loads, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260114-3.15.0a4+-1857a40/bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.158x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.22x