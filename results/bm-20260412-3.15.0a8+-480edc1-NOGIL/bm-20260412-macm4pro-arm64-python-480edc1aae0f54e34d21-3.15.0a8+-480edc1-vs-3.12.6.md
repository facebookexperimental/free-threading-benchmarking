# Results vs. 3.12.6

- fork: python
- ref: 480edc1aae0f54e34d21
- machine: darwin-arm64
- commit hash: 480edc1
- commit date: 2026-04-12
- overall geometric mean: 1.090x faster
- HPT reliability: 99.53%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 125 ms: 1.10x slower                                                     |
| docutils       | 1.02 sec                                                 | 995 ms: 1.03x faster                                                     |
| sphinx         | 434 ms                                                   | 422 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 251 ms: 1.91x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.87x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 241 ms: 1.85x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 111 ms: 1.55x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 118 ms: 1.52x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.48x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 269 ms: 1.24x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                     |
| async_generators                 | 206 ms                                                   | 189 ms: 1.10x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.6 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.6 ms: 2.91x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.0 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.1 ms: 1.07x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.1 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.27 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.5 ms: 1.37x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.3 ms: 1.19x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                    |
| tomli_loads          | 957 ms                                                   | 894 ms: 1.07x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.6 us: 1.07x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.82 ms: 1.23x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.13 ms: 1.25x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.24x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.6 ms: 1.04x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 12.0 ms: 1.14x slower                                                    |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                    |
| mako            | 4.77 ms                                                  | 5.60 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.15 ms: 5.00x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 809 us: 2.48x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 251 ms: 1.91x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.87x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 241 ms: 1.85x faster                                                     |
| mdp                              | 1.09 sec                                                 | 606 ms: 1.80x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 514 us: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 111 ms: 1.55x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 118 ms: 1.52x faster                                                     |
| deepcopy                         | 161 us                                                   | 109 us: 1.48x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.48x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.1 us: 1.40x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.5 ms: 1.37x faster                                                    |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 269 ms: 1.24x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.23x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 800 ns: 1.21x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.15 us: 1.21x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.3 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 43.6 ns: 1.17x faster                                                    |
| go                               | 70.0 ms                                                  | 60.2 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 999 ms: 1.12x faster                                                     |
| pyflate                          | 216 ms                                                   | 194 ms: 1.12x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.7 ms: 1.10x faster                                                    |
| async_generators                 | 206 ms                                                   | 189 ms: 1.10x faster                                                     |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 50.0 ms: 1.09x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.37 us: 1.09x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                     |
| pycparser                        | 497 ms                                                   | 460 ms: 1.08x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.62 us: 1.07x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 894 ms: 1.07x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 51.1 ms: 1.07x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.1 ms: 1.06x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.4 ms: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.1 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.27 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| generators                       | 21.9 ms                                                  | 21.3 ms: 1.03x faster                                                    |
| sphinx                           | 434 ms                                                   | 422 ms: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 995 ms: 1.03x faster                                                     |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.12 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 334 ms: 1.02x slower                                                     |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.7 us: 1.02x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 685 ms: 1.03x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 22.6 ms: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.3 ms: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.6 ms: 1.04x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.6 ms: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.19 ms: 1.05x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.6 ms: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.0 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 61.2 ms: 1.06x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.6 us: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 55.4 ms: 1.08x slower                                                    |
| thrift                           | 322 us                                                   | 350 us: 1.09x slower                                                     |
| 2to3                             | 114 ms                                                   | 125 ms: 1.10x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.28 ms: 1.10x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                     |
| shortest_path                    | 219 ms                                                   | 250 ms: 1.14x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 12.0 ms: 1.14x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 44.5 ms: 1.15x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.05 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.8 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.60 ms: 1.17x slower                                                    |
| connected_components             | 201 ms                                                   | 244 ms: 1.21x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 48.3 ms: 1.22x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.82 ms: 1.23x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.13 ms: 1.25x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 566 us: 1.35x slower                                                     |
| many_optionals                   | 195 us                                                   | 270 us: 1.38x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.6 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.6 ms: 2.91x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (2): dask, html5lib
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260412-3.15.0a8+-480edc1-NOGIL/bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.090x faster

# HPT report

- Reliability score: 99.53% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.38x