# Results vs. 3.13.0rc2

- fork: python
- ref: cdfdf7bb73a5751ecec7
- machine: darwin-arm64
- commit hash: cdfdf7b
- commit date: 2026-10-08
- overall geometric mean: 1.069x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| docutils       | 1.05 sec                                                       | 941 ms: 1.11x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                   |
| sphinx         | 409 ms                                                         | 397 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 305 ms: 1.72x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 332 ms: 1.57x faster                                                    |
| async_generators                 | 193 ms                                                         | 146 ms: 1.32x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 312 ms: 1.24x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 331 ms: 1.22x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 119 ms: 1.19x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.75 ms: 1.10x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 277 ms: 1.06x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 175 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 288 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 260 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 153 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.56x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                   |
| nbody          | 42.5 ms                                                        | 40.5 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.30 ms: 1.24x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 89.3 ms: 1.06x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 54.3 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.55 ms: 1.31x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 806 ms: 1.24x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.3 ms: 1.07x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 95.2 us: 1.04x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 138 us: 1.06x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 68.1 ms: 1.09x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.09 ms: 1.05x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.62 ms: 1.11x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.56 ms: 1.03x slower                                                   |
| django_template | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 507 ms: 2.09x faster                                                    |
| pylint                           | 106 ms                                                         | 55.5 ms: 1.90x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 305 ms: 1.72x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 332 ms: 1.57x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.07 ms: 1.54x faster                                                   |
| deepcopy                         | 145 us                                                         | 95.7 us: 1.52x faster                                                   |
| k_core                           | 1.46 sec                                                       | 979 ms: 1.49x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.43x faster                                                   |
| go                               | 72.6 ms                                                        | 52.2 ms: 1.39x faster                                                   |
| async_generators                 | 193 ms                                                         | 146 ms: 1.32x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.55 ms: 1.31x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 49.4 us: 1.31x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 50.7 ms: 1.26x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 312 ms: 1.24x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 806 ms: 1.24x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.30 ms: 1.24x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 331 ms: 1.22x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 819 us: 1.21x faster                                                    |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 119 ms: 1.19x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                   |
| fannkuch                         | 179 ms                                                         | 160 ms: 1.12x faster                                                    |
| float                            | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                   |
| docutils                         | 1.05 sec                                                       | 941 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.75 ms: 1.10x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.2 ms: 1.10x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| richards                         | 22.1 ms                                                        | 20.3 ms: 1.08x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 115 ms: 1.08x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.08x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.65 ms: 1.07x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.91 ms: 1.07x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.3 ms: 1.07x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.2 ms: 1.07x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.88 ms: 1.07x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 35.1 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 277 ms: 1.06x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 89.3 ms: 1.06x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.06x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 175 ms: 1.05x faster                                                    |
| nbody                            | 42.5 ms                                                        | 40.5 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 288 ms: 1.05x faster                                                    |
| json                             | 1.94 ms                                                        | 1.86 ms: 1.05x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 95.2 us: 1.04x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 308 ms: 1.04x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 42.0 ms: 1.04x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.17 us: 1.03x faster                                                   |
| sphinx                           | 409 ms                                                         | 397 ms: 1.03x faster                                                    |
| comprehensions                   | 6.80 us                                                        | 6.64 us: 1.03x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.35 ms: 1.02x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 634 ms: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 930 ns: 1.02x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.76 ms: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.00x slower                                                   |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.00x slower                                                    |
| connected_components             | 208 ms                                                         | 209 ms: 1.01x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 416 us: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.1 ms: 1.02x slower                                                   |
| pycparser                        | 470 ms                                                         | 484 ms: 1.03x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.0 ms: 1.03x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.56 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 98.9 ms: 1.04x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.3 ns: 1.04x slower                                                   |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 54.9 ms: 1.05x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.09 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.06x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 138 us: 1.06x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 46.1 ms: 1.08x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.1 ms: 1.09x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 68.1 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 36.9 ms: 1.10x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.62 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.3 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.6 ms: 1.18x slower                                                   |
| many_optionals                   | 200 us                                                         | 239 us: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 260 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 153 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.56x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                            |

Benchmark hidden because not significant (1): thrift
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.069x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x