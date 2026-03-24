# Results vs. 3.13.0rc2

- fork: python
- ref: bcff99cb3f3b887a08c4
- machine: darwin-arm64
- commit hash: bcff99c
- commit date: 2026-03-23
- overall geometric mean: 1.021x faster
- HPT reliability: 56.78%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| docutils       | 1.05 sec                                                       | 993 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 417 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 238 ms: 2.19x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 236 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 48.2 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.3 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.00x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.5 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.25 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.8 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.0 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.87 ms: 1.20x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.9 ms: 1.18x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 858 ms: 1.16x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.4 ms: 1.07x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.04x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.83 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.14 ms: 1.20x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.4 ms: 1.05x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| mako            | 4.41 ms                                                        | 5.51 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 808 us: 2.53x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 238 ms: 2.19x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 505 us: 1.97x faster                                                     |
| mdp                              | 1.06 sec                                                       | 606 ms: 1.75x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 236 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.10 ms: 1.53x faster                                                    |
| k_core                           | 1.46 sec                                                       | 986 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 106 us: 1.37x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| go                               | 72.6 ms                                                        | 59.4 ms: 1.22x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.87 ms: 1.20x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 792 ns: 1.20x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 53.8 ms: 1.19x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.9 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 858 ms: 1.16x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.25 ms: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.14x faster                                                    |
| float                            | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.11x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.4 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 993 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.99 ms: 1.03x faster                                                    |
| pycparser                        | 470 ms                                                         | 460 ms: 1.02x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.00x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| dask                             | 525 ms                                                         | 529 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                    |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.8 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 327 ms: 1.01x slower                                                     |
| sphinx                           | 409 ms                                                         | 417 ms: 1.02x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 665 ms: 1.02x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 41.7 ns: 1.03x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.03x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.04x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.4 ms: 1.05x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.1 ms: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.38 us: 1.06x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.0 ms: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.61 us: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.10 ms: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.8 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 40.5 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.9 ms: 1.10x slower                                                    |
| thrift                           | 309 us                                                         | 342 us: 1.11x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 48.2 ms: 1.12x slower                                                    |
| shortest_path                    | 225 ms                                                         | 252 ms: 1.12x slower                                                     |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.12x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 72.7 us: 1.12x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.4 ms: 1.13x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 49.6 ms: 1.13x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.83 ms: 1.14x slower                                                    |
| raytrace                         | 109 ms                                                         | 126 ms: 1.16x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.4 ms: 1.16x slower                                                    |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 61.7 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.14 ms: 1.20x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.14 ms: 1.20x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.29 us: 1.22x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.5 ms: 1.23x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 52.7 ms: 1.23x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.24x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.7 ms: 1.24x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.51 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 44.3 ms: 1.32x slower                                                    |
| many_optionals                   | 200 us                                                         | 265 us: 1.32x slower                                                     |
| nbody                            | 42.5 ms                                                        | 56.5 ms: 1.33x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 567 us: 1.38x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.3 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260323-3.15.0a7+-bcff99c-NOGIL/bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.021x faster

# HPT report

- Reliability score: 56.78% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.32x