# Results vs. 3.12.6

- fork: python
- ref: d19de375a204c74ab5f3
- machine: darwin-arm64
- commit hash: d19de37
- commit date: 2026-03-11
- overall geometric mean: 1.105x faster
- HPT reliability: 99.74%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| docutils       | 1.02 sec                                                 | 987 ms: 1.04x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| sphinx         | 434 ms                                                   | 420 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 244 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 236 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 238 ms: 1.88x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.85x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                     |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.1 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.9 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.6 ms: 1.33x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 56.9 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.3 ms: 1.09x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.15 ms: 1.05x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.4 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.4 ms: 1.28x faster                                                    |
| tomli_loads          | 957 ms                                                   | 851 ms: 1.13x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 62.2 ms: 1.09x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 105 us: 1.02x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.91 ms: 1.24x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.23 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.25x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.1 ms: 1.06x slower                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| mako            | 4.77 ms                                                  | 5.57 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.03 ms: 5.15x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 800 us: 2.51x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 244 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 236 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 238 ms: 1.88x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.85x faster                                                     |
| mdp                              | 1.09 sec                                                 | 603 ms: 1.81x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 504 us: 1.65x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.57x faster                                                     |
| deepcopy                         | 161 us                                                   | 105 us: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| float                            | 37.9 ms                                                  | 28.6 ms: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.29x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.4 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 787 ns: 1.23x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.19 us: 1.20x faster                                                    |
| go                               | 70.0 ms                                                  | 59.1 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.2 ns: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| pyflate                          | 216 ms                                                   | 190 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 987 ms: 1.13x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.13x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 851 ms: 1.13x faster                                                     |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.34 us: 1.10x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.7 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 455 ms: 1.09x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 62.2 ms: 1.09x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.1 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 50.3 ms: 1.09x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.1 ms: 1.09x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.0 ms: 1.07x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.7 ms: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.07x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.15 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.4 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.04x faster                                                     |
| docutils                         | 1.02 sec                                                 | 987 ms: 1.04x faster                                                     |
| sphinx                           | 434 ms                                                   | 420 ms: 1.03x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 670 ms: 1.01x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.10 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.1 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| richards                         | 22.4 ms                                                  | 22.8 ms: 1.02x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 25.9 ms: 1.02x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 105 us: 1.02x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.13 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.8 us: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.1 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.13 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                     |
| nbody                            | 54.2 ms                                                  | 56.9 ms: 1.05x slower                                                    |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.1 ms: 1.06x slower                                                    |
| thrift                           | 322 us                                                   | 340 us: 1.06x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.9 ms: 1.06x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 56.2 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.0 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| shortest_path                    | 219 ms                                                   | 252 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.5 ms: 1.16x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.57 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.6 ms: 1.17x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.91 ms: 1.24x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.23 ms: 1.27x slower                                                    |
| many_optionals                   | 195 us                                                   | 262 us: 1.34x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 584 us: 1.39x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.6 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.9 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (2): pprint_safe_repr, dask
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: asyncio_websockets, chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260311-3.15.0a7+-d19de37-NOGIL/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.105x faster

# HPT report

- Reliability score: 99.74% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.38x