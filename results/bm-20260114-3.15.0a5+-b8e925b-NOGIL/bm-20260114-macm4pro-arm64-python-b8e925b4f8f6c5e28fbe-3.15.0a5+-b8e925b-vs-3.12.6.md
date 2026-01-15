# Results vs. 3.12.6

- fork: python
- ref: b8e925b4f8f6c5e28fbe
- machine: darwin-arm64
- commit hash: b8e925b
- commit date: 2026-01-14
- overall geometric mean: 1.084x faster
- HPT reliability: 98.30%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.00x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| sphinx         | 434 ms                                                   | 430 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 253 ms: 1.90x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.83x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.56x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 261 ms: 1.29x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.24x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                     |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.7 ms: 1.05x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.8 ms: 2.95x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.1 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.2 ms: 1.07x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.1 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.35 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.0 ms: 1.17x faster                                                    |
| tomli_loads          | 957 ms                                                   | 894 ms: 1.07x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.98 ms: 1.07x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.8 ms: 1.03x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.06x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 149 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.32 ms: 1.28x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.27x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.9 ms: 1.10x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                    |
| django_template | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| mako            | 4.77 ms                                                  | 5.55 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.17 ms: 4.98x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 824 us: 2.44x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 253 ms: 1.90x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.83x faster                                                     |
| mdp                              | 1.09 sec                                                 | 601 ms: 1.82x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 520 us: 1.60x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.56x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.54x faster                                                     |
| deepcopy                         | 161 us                                                   | 109 us: 1.48x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.45x faster                                                    |
| float                            | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 261 ms: 1.29x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.24x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 58.0 ms: 1.17x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 831 ns: 1.16x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.48 us: 1.16x faster                                                    |
| go                               | 70.0 ms                                                  | 60.6 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 44.5 ns: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                   |
| raytrace                         | 145 ms                                                   | 128 ms: 1.13x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.13x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.00 sec: 1.11x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.1 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                     |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 49.9 ms: 1.09x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 894 ms: 1.07x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.98 ms: 1.07x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.2 ms: 1.07x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.43 us: 1.06x faster                                                    |
| pylint                           | 128 ms                                                   | 122 ms: 1.05x faster                                                     |
| pycparser                        | 497 ms                                                   | 473 ms: 1.05x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.68 us: 1.05x faster                                                    |
| generators                       | 21.9 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.1 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.8 ms: 1.03x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.35 ms: 1.03x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.3 ms: 1.02x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 42.9 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.05 ms: 1.01x faster                                                    |
| sphinx                           | 434 ms                                                   | 430 ms: 1.01x faster                                                     |
| fannkuch                         | 176 ms                                                   | 175 ms: 1.00x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.00x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 71.5 us: 1.01x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 333 ms: 1.02x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.7 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.25 ms: 1.03x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 685 ms: 1.03x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.7 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.5 ms: 1.05x slower                                                    |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                     |
| nbody                            | 54.2 ms                                                  | 57.1 ms: 1.05x slower                                                    |
| thrift                           | 322 us                                                   | 340 us: 1.06x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 26.9 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.06x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 149 us: 1.07x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 41.6 ms: 1.07x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.7 ms: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 55.5 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.9 ms: 1.10x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.03 ms: 1.16x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.55 ms: 1.16x slower                                                    |
| shortest_path                    | 219 ms                                                   | 255 ms: 1.16x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 47.2 ms: 1.19x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.7 ms: 1.19x slower                                                    |
| connected_components             | 201 ms                                                   | 247 ms: 1.23x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.32 ms: 1.28x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 562 us: 1.34x slower                                                     |
| many_optionals                   | 195 us                                                   | 272 us: 1.39x slower                                                     |
| coverage                         | 26.9 ms                                                  | 39.4 ms: 1.47x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.8 ms: 2.95x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260114-3.15.0a5+-b8e925b-NOGIL/bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.084x faster

# HPT report

- Reliability score: 98.30% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.35x