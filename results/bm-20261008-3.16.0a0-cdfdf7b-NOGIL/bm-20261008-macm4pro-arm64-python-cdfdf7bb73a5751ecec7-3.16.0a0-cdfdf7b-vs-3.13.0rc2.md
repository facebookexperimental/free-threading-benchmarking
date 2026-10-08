# Results vs. 3.13.0rc2

- fork: python
- ref: cdfdf7bb73a5751ecec7
- machine: darwin-arm64
- commit hash: cdfdf7b
- commit date: 2026-10-08
- overall geometric mean: 1.022x slower
- HPT reliability: 94.57%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 130 ms: 1.16x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| sphinx         | 409 ms                                                         | 443 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 295 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 293 ms: 1.78x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 294 ms: 1.38x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 307 ms: 1.26x faster                                                    |
| async_generators                 | 193 ms                                                         | 161 ms: 1.20x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 180 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 293 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 299 ms: 1.02x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 125 ms: 1.03x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 139 ms: 1.05x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 50.1 ms: 1.16x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 12.7 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 274 ms: 1.32x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 163 ms: 1.59x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 113 ms: 3.92x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (2): async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| float          | 31.4 ms                                                        | 33.0 ms: 1.05x slower                                                   |
| nbody          | 42.5 ms                                                        | 59.0 ms: 1.39x slower                                                   |
| Geometric mean | (ref)                                                          | 1.13x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.34 ms: 1.20x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 91.2 ms: 1.04x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 64.3 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.75 ms: 1.24x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 891 ms: 1.12x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.5 ms: 1.11x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.2 ms: 1.05x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 38.7 ms: 1.08x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.09x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 29.8 ms: 1.17x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 155 us: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.33 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.20x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.77 ms: 1.31x slower                                                   |
| django_template | 12.5 ms                                                        | 17.0 ms: 1.37x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.34x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 777 us: 2.63x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 492 us: 2.02x faster                                                    |
| pylint                           | 106 ms                                                         | 53.6 ms: 1.97x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 295 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 293 ms: 1.78x faster                                                    |
| mdp                              | 1.06 sec                                                       | 599 ms: 1.77x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                  |
| subparsers                       | 6.26 ms                                                        | 4.36 ms: 1.44x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 294 ms: 1.38x faster                                                    |
| deepcopy                         | 145 us                                                         | 107 us: 1.35x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 307 ms: 1.26x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.75 ms: 1.24x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 787 ns: 1.20x faster                                                    |
| async_generators                 | 193 ms                                                         | 161 ms: 1.20x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.34 ms: 1.20x faster                                                   |
| go                               | 72.6 ms                                                        | 60.9 ms: 1.19x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 14.6 us: 1.13x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 891 ms: 1.12x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 57.7 us: 1.12x faster                                                   |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.5 ms: 1.11x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 58.1 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                  |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 59.2 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 91.2 ms: 1.04x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 180 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 293 ms: 1.03x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.3 ms: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.01x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| pycparser                        | 470 ms                                                         | 479 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 299 ms: 1.02x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.15 ms: 1.03x slower                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 125 ms: 1.03x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.03x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 139 ms: 1.05x slower                                                    |
| float                            | 31.4 ms                                                        | 33.0 ms: 1.05x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 38.7 ms: 1.08x slower                                                   |
| sphinx                           | 409 ms                                                         | 443 ms: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.18 ms: 1.09x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.09x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 354 ms: 1.10x slower                                                    |
| shortest_path                    | 225 ms                                                         | 249 ms: 1.11x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.47 us: 1.11x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.73 us: 1.12x slower                                                   |
| richards                         | 22.1 ms                                                        | 24.7 ms: 1.12x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 48.9 ms: 1.12x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.7 ms: 1.13x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.9 ms: 1.13x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                   |
| thrift                           | 309 us                                                         | 351 us: 1.14x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 740 ms: 1.14x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.26 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.7 ms: 1.15x slower                                                   |
| connected_components             | 208 ms                                                         | 240 ms: 1.15x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 50.1 ms: 1.16x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 43.3 ms: 1.16x slower                                                   |
| 2to3                             | 112 ms                                                         | 130 ms: 1.16x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.3 ms: 1.17x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 29.8 ms: 1.17x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 12.7 ms: 1.18x slower                                                   |
| chaos                            | 24.3 ms                                                        | 28.8 ms: 1.19x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 155 us: 1.19x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 48.5 ns: 1.19x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.33 ms: 1.23x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.24x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 41.6 ms: 1.24x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.81 ms: 1.25x slower                                                   |
| raytrace                         | 109 ms                                                         | 136 ms: 1.25x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.58 us: 1.26x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.5 ms: 1.30x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.77 ms: 1.31x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 274 ms: 1.32x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 64.3 ms: 1.34x slower                                                   |
| many_optionals                   | 200 us                                                         | 269 us: 1.34x slower                                                    |
| django_template                  | 12.5 ms                                                        | 17.0 ms: 1.37x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 568 us: 1.38x slower                                                    |
| nbody                            | 42.5 ms                                                        | 59.0 ms: 1.39x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 63.2 ms: 1.48x slower                                                   |
| generators                       | 15.7 ms                                                        | 23.5 ms: 1.50x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 163 ms: 1.59x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 113 ms: 3.92x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (4): html5lib, async_tree_none, json_loads, async_tree_memoization
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.022x slower

# HPT report

- Reliability score: 94.57% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.26x