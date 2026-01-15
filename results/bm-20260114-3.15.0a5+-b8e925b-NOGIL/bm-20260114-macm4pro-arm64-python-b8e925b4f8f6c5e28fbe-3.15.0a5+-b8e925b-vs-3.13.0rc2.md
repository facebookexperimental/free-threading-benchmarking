# Results vs. 3.13.0rc2

- fork: python
- ref: b8e925b4f8f6c5e28fbe
- machine: darwin-arm64
- commit hash: b8e925b
- commit date: 2026-01-14
- overall geometric mean: 1.005x faster
- HPT reliability: 72.49%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.11x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.03x slower                                                    |
| sphinx         | 409 ms                                                         | 430 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 245 ms: 2.12x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.21x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 270 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.7 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.8 ms: 3.28x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.7 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                     |
| nbody          | 42.5 ms                                                        | 57.1 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.35 ms: 1.14x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.1 ms: 1.02x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.2 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.0 ms: 1.18x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.98 ms: 1.17x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 894 ms: 1.12x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.0 ms: 1.08x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.8 ms: 1.06x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 149 us: 1.14x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.32 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.20x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.9 ms: 1.12x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.5 ms: 1.16x slower                                                    |
| mako            | 4.41 ms                                                        | 5.55 ms: 1.26x slower                                                    |
| django_template | 12.5 ms                                                        | 15.8 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 824 us: 2.48x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 245 ms: 2.12x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 520 us: 1.91x faster                                                     |
| mdp                              | 1.06 sec                                                       | 601 ms: 1.76x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.17 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                   |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.30x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.21x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.21x faster                                                     |
| go                               | 72.6 ms                                                        | 60.6 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.0 ms: 1.18x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.98 ms: 1.17x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.1 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.35 ms: 1.14x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 831 ns: 1.14x faster                                                     |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 894 ms: 1.12x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                    |
| float                            | 31.4 ms                                                        | 28.7 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 270 ms: 1.09x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 58.0 ms: 1.08x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                    |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                     |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.03 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 473 ms: 1.01x slower                                                     |
| dask                             | 525 ms                                                         | 529 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 96.1 ms: 1.02x slower                                                    |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 333 ms: 1.04x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| sphinx                           | 409 ms                                                         | 430 ms: 1.05x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 685 ms: 1.05x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.8 ms: 1.06x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.5 ms: 1.07x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.2 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.43 us: 1.09x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.9 ms: 1.09x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.68 us: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.5 ns: 1.09x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.7 ms: 1.10x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.25 ms: 1.10x slower                                                    |
| thrift                           | 309 us                                                         | 340 us: 1.10x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.7 ms: 1.10x slower                                                    |
| 2to3                             | 112 ms                                                         | 123 ms: 1.11x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 71.5 us: 1.11x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.9 ms: 1.12x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                    |
| shortest_path                    | 225 ms                                                         | 255 ms: 1.13x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 49.9 ms: 1.14x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.14x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 42.9 ms: 1.15x slower                                                    |
| pylint                           | 106 ms                                                         | 122 ms: 1.15x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.05 ms: 1.15x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.5 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| chaos                            | 24.3 ms                                                        | 28.3 ms: 1.17x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.17x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 61.7 ms: 1.18x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.18x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 56.7 ms: 1.18x slower                                                    |
| connected_components             | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.32 ms: 1.23x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 41.6 ms: 1.24x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.48 us: 1.25x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.2 ms: 1.25x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.55 ms: 1.26x slower                                                    |
| coverage                         | 31.2 ms                                                        | 39.4 ms: 1.26x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.8 ms: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 55.5 ms: 1.30x slower                                                    |
| generators                       | 15.7 ms                                                        | 21.0 ms: 1.34x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.1 ms: 1.34x slower                                                    |
| many_optionals                   | 200 us                                                         | 272 us: 1.36x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 562 us: 1.37x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.8 ms: 3.28x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (1): coroutines
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260114-3.15.0a5+-b8e925b-NOGIL/bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 72.49% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x