# Results vs. 3.13.0rc2

- fork: python
- ref: a6b4aa687cd9f8f95e3b
- machine: darwin-arm64
- commit hash: a6b4aa6
- commit date: 2026-10-14
- overall geometric mean: 1.019x slower
- HPT reliability: 91.41%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 129 ms: 1.15x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                      |
| html5lib       | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                       |
| sphinx         | 409 ms                                                         | 445 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                          | 1.05x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 295 ms: 1.77x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 298 ms: 1.76x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 297 ms: 1.36x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 307 ms: 1.26x faster                                                        |
| async_generators                 | 193 ms                                                         | 159 ms: 1.21x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 181 ms: 1.02x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 295 ms: 1.02x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 125 ms: 1.03x slower                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 302 ms: 1.03x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 236 ms: 1.05x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 140 ms: 1.06x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 12.1 ms: 1.13x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 50.4 ms: 1.17x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 276 ms: 1.33x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 164 ms: 1.60x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 114 ms: 3.94x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.03x slower                                                                |

Benchmark hidden because not significant (2): async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                        |
| float          | 31.4 ms                                                        | 33.1 ms: 1.05x slower                                                       |
| nbody          | 42.5 ms                                                        | 57.5 ms: 1.35x slower                                                       |
| Geometric mean | (ref)                                                          | 1.12x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.22 ms: 1.16x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 92.4 ms: 1.02x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 64.5 ms: 1.35x slower                                                       |
| Geometric mean | (ref)                                                          | 1.02x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 868 ms: 1.15x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.9 ms: 1.13x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                       |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.02x slower                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 39.0 ms: 1.09x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 30.0 ms: 1.18x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 154 us: 1.18x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.96 ms: 1.15x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 7.31 ms: 1.23x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.19x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.76 ms: 1.31x slower                                                       |
| django_template | 12.5 ms                                                        | 16.9 ms: 1.36x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.33x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 778 us: 2.62x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 474 us: 2.10x faster                                                        |
| pylint                           | 106 ms                                                         | 53.0 ms: 1.99x faster                                                       |
| mdp                              | 1.06 sec                                                       | 590 ms: 1.79x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 295 ms: 1.77x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 298 ms: 1.76x faster                                                        |
| k_core                           | 1.46 sec                                                       | 997 ms: 1.47x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.32 ms: 1.45x faster                                                       |
| async_tree_io_tg                 | 405 ms                                                         | 297 ms: 1.36x faster                                                        |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 307 ms: 1.26x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                       |
| async_generators                 | 193 ms                                                         | 159 ms: 1.21x faster                                                        |
| go                               | 72.6 ms                                                        | 60.0 ms: 1.21x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 13.9 us: 1.19x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 803 ns: 1.18x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.22 ms: 1.16x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 868 ms: 1.15x faster                                                        |
| pyflate                          | 222 ms                                                         | 196 ms: 1.14x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 57.3 us: 1.13x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.9 ms: 1.13x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 58.0 ms: 1.10x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                      |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 19.2 ms: 1.03x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 181 ms: 1.02x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 92.4 ms: 1.02x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 295 ms: 1.02x faster                                                        |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                       |
| fannkuch                         | 179 ms                                                         | 176 ms: 1.01x faster                                                        |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                      |
| pycparser                        | 470 ms                                                         | 478 ms: 1.02x slower                                                        |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.02x slower                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 125 ms: 1.03x slower                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 302 ms: 1.03x slower                                                        |
| telco                            | 3.07 ms                                                        | 3.19 ms: 1.04x slower                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 236 ms: 1.05x slower                                                        |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                        |
| float                            | 31.4 ms                                                        | 33.1 ms: 1.05x slower                                                       |
| async_tree_none_tg               | 133 ms                                                         | 140 ms: 1.06x slower                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 8.13 ms: 1.08x slower                                                       |
| sphinx                           | 409 ms                                                         | 445 ms: 1.09x slower                                                        |
| richards                         | 22.1 ms                                                        | 24.1 ms: 1.09x slower                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 39.0 ms: 1.09x slower                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 352 ms: 1.09x slower                                                        |
| logging_format                   | 2.45 us                                                        | 2.69 us: 1.10x slower                                                       |
| logging_simple                   | 2.24 us                                                        | 2.47 us: 1.10x slower                                                       |
| shortest_path                    | 225 ms                                                         | 248 ms: 1.11x slower                                                        |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                        |
| meteor_contest                   | 47.9 ms                                                        | 53.3 ms: 1.11x slower                                                       |
| richards_super                   | 24.7 ms                                                        | 27.6 ms: 1.12x slower                                                       |
| thrift                           | 309 us                                                         | 347 us: 1.12x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 12.1 ms: 1.13x slower                                                       |
| hexiom                           | 2.85 ms                                                        | 3.22 ms: 1.13x slower                                                       |
| spectral_norm                    | 43.7 ms                                                        | 49.5 ms: 1.13x slower                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.9 ms: 1.13x slower                                                       |
| pprint_pformat                   | 650 ms                                                         | 738 ms: 1.14x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 43.0 ms: 1.14x slower                                                       |
| connected_components             | 208 ms                                                         | 239 ms: 1.15x slower                                                        |
| 2to3                             | 112 ms                                                         | 129 ms: 1.15x slower                                                        |
| python_startup                   | 8.63 ms                                                        | 9.96 ms: 1.15x slower                                                       |
| nqueens                          | 37.2 ms                                                        | 43.0 ms: 1.16x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 60.9 ms: 1.16x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 50.4 ms: 1.17x slower                                                       |
| xml_etree_process                | 25.4 ms                                                        | 30.0 ms: 1.18x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 154 us: 1.18x slower                                                        |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                        |
| chaos                            | 24.3 ms                                                        | 28.9 ms: 1.19x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 49.1 ns: 1.21x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 41.0 ms: 1.22x slower                                                       |
| comprehensions                   | 6.80 us                                                        | 8.32 us: 1.22x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 7.31 ms: 1.23x slower                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.24x slower                                                       |
| deltablue                        | 1.45 ms                                                        | 1.80 ms: 1.24x slower                                                       |
| raytrace                         | 109 ms                                                         | 138 ms: 1.26x slower                                                        |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                        |
| coverage                         | 31.2 ms                                                        | 40.3 ms: 1.29x slower                                                       |
| mako                             | 4.41 ms                                                        | 5.76 ms: 1.31x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 276 ms: 1.33x slower                                                        |
| regex_compile                    | 47.9 ms                                                        | 64.5 ms: 1.35x slower                                                       |
| nbody                            | 42.5 ms                                                        | 57.5 ms: 1.35x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.9 ms: 1.36x slower                                                       |
| bench_thread_pool                | 412 us                                                         | 577 us: 1.40x slower                                                        |
| generators                       | 15.7 ms                                                        | 23.6 ms: 1.50x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 164 ms: 1.60x slower                                                        |
| scimark_lu                       | 42.8 ms                                                        | 68.4 ms: 1.60x slower                                                       |
| async_tree_eager_tg              | 28.9 ms                                                        | 114 ms: 3.94x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                                |

Benchmark hidden because not significant (3): json, async_tree_none, async_tree_memoization
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261014-3.16.0a1+dev-a6b4aa6-NOGIL/bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.019x slower

# HPT report

- Reliability score: 91.41% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.25x