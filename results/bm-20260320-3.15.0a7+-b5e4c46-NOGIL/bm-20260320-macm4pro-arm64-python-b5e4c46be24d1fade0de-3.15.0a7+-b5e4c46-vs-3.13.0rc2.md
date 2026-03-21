# Results vs. 3.13.0rc2

- fork: python
- ref: b5e4c46be24d1fade0de
- machine: darwin-arm64
- commit hash: b5e4c46
- commit date: 2026-03-20
- overall geometric mean: 1.015x faster
- HPT reliability: 62.24%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.10x slower                                                     |
| docutils       | 1.05 sec                                                       | 995 ms: 1.05x faster                                                     |
| sphinx         | 409 ms                                                         | 420 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 237 ms: 2.19x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 236 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 187 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.3 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.7 ms: 3.20x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                     |
| nbody          | 42.5 ms                                                        | 57.2 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 50.8 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.7 ms: 1.19x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 858 ms: 1.17x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.99 ms: 1.16x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.90 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.19 ms: 1.21x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| mako            | 4.41 ms                                                        | 5.55 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 805 us: 2.53x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 237 ms: 2.19x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 502 us: 1.98x faster                                                     |
| mdp                              | 1.06 sec                                                       | 611 ms: 1.73x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 236 ms: 1.72x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.11 ms: 1.52x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                     |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                   |
| deepcopy                         | 145 us                                                         | 106 us: 1.37x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| go                               | 72.6 ms                                                        | 60.2 ms: 1.21x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.7 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 810 ns: 1.17x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 858 ms: 1.17x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.99 ms: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.8 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.08x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| docutils                         | 1.05 sec                                                       | 995 ms: 1.05x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                    |
| async_generators                 | 193 ms                                                         | 187 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| pycparser                        | 470 ms                                                         | 463 ms: 1.01x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.04 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                     |
| dask                             | 525 ms                                                         | 529 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 329 ms: 1.02x slower                                                     |
| sphinx                           | 409 ms                                                         | 420 ms: 1.03x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 127 ms: 1.03x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 673 ms: 1.04x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.8 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.07x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.38 us: 1.07x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.6 ms: 1.07x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.5 ns: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.7 ms: 1.08x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.65 us: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.18 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.10x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.3 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.0 ms: 1.10x slower                                                    |
| thrift                           | 309 us                                                         | 342 us: 1.11x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 41.2 ms: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 250 ms: 1.11x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.19 ms: 1.12x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.3 ms: 1.12x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 72.7 us: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.14x slower                                                    |
| pylint                           | 106 ms                                                         | 120 ms: 1.14x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.90 ms: 1.15x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.5 ms: 1.16x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.7 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| raytrace                         | 109 ms                                                         | 127 ms: 1.16x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 61.7 ms: 1.18x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.12 ms: 1.19x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.19 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.27 us: 1.22x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.7 ms: 1.23x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 52.9 ms: 1.24x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.55 ms: 1.26x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.1 ms: 1.28x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 44.8 ms: 1.33x slower                                                    |
| many_optionals                   | 200 us                                                         | 268 us: 1.34x slower                                                     |
| nbody                            | 42.5 ms                                                        | 57.2 ms: 1.35x slower                                                    |
| generators                       | 15.7 ms                                                        | 21.2 ms: 1.35x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 571 us: 1.39x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.7 ms: 3.20x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (3): html5lib, coroutines, fannkuch
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260320-3.15.0a7+-b5e4c46-NOGIL/bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.015x faster

# HPT report

- Reliability score: 62.24% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.32x