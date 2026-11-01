# Results vs. 3.13.0rc2

- fork: python
- ref: 410fdda081ba1ca95be0
- machine: darwin-arm64
- commit hash: 410fdda
- commit date: 2026-10-31
- overall geometric mean: 1.010x faster
- HPT reliability: 73.08%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.11x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                      |
| html5lib       | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                       |
| sphinx         | 409 ms                                                         | 436 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                          | 1.03x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 285 ms: 1.82x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 289 ms: 1.81x faster                                                        |
| async_generators                 | 193 ms                                                         | 110 ms: 1.75x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 289 ms: 1.40x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 297 ms: 1.30x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 181 ms: 1.07x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 287 ms: 1.05x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 178 ms: 1.05x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 139 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 227 ms: 1.01x slower                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 124 ms: 1.02x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 11.8 ms: 1.10x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 48.8 ms: 1.13x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 263 ms: 1.26x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 161 ms: 1.57x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 108 ms: 3.74x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                                |

Benchmark hidden because not significant (3): async_tree_memoization, async_tree_cpu_io_mixed, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 157 ms: 1.06x faster                                                        |
| float          | 31.4 ms                                                        | 32.7 ms: 1.04x slower                                                       |
| nbody          | 42.5 ms                                                        | 58.3 ms: 1.37x slower                                                       |
| Geometric mean | (ref)                                                          | 1.10x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 8.92 ms: 1.20x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 88.1 ms: 1.07x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 62.5 ms: 1.30x slower                                                       |
| Geometric mean | (ref)                                                          | 1.05x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.65 ms: 1.27x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 865 ms: 1.16x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 57.6 ms: 1.08x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 37.8 ms: 1.06x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.08x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 28.8 ms: 1.14x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 155 us: 1.19x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.78 ms: 1.02x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.80 ms: 1.14x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.40 ms: 1.22x slower                                                       |
| django_template | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.27x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 771 us: 2.65x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 455 us: 2.19x faster                                                        |
| pylint                           | 106 ms                                                         | 50.5 ms: 2.09x faster                                                       |
| mdp                              | 1.06 sec                                                       | 569 ms: 1.86x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 285 ms: 1.82x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 289 ms: 1.81x faster                                                        |
| async_generators                 | 193 ms                                                         | 110 ms: 1.75x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.22 ms: 1.48x faster                                                       |
| k_core                           | 1.46 sec                                                       | 994 ms: 1.47x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 289 ms: 1.40x faster                                                        |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 297 ms: 1.30x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.65 ms: 1.27x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| go                               | 72.6 ms                                                        | 59.3 ms: 1.22x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 53.6 us: 1.21x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 8.92 ms: 1.20x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 13.9 us: 1.18x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 804 ns: 1.18x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 865 ms: 1.16x faster                                                        |
| pyflate                          | 222 ms                                                         | 193 ms: 1.15x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.11x faster                                                      |
| scimark_sor                      | 64.0 ms                                                        | 57.7 ms: 1.11x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.10x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 57.6 ms: 1.08x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 88.1 ms: 1.07x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 181 ms: 1.07x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                       |
| pidigits                         | 166 ms                                                         | 157 ms: 1.06x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 287 ms: 1.05x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 178 ms: 1.05x faster                                                        |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                       |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                      |
| html5lib                         | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 139 ms: 1.02x faster                                                        |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                       |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.01x faster                                                       |
| pycparser                        | 470 ms                                                         | 467 ms: 1.01x faster                                                        |
| fannkuch                         | 179 ms                                                         | 179 ms: 1.00x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 227 ms: 1.01x slower                                                        |
| python_startup                   | 8.63 ms                                                        | 8.78 ms: 1.02x slower                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 124 ms: 1.02x slower                                                        |
| float                            | 31.4 ms                                                        | 32.7 ms: 1.04x slower                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 37.8 ms: 1.06x slower                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.97 ms: 1.06x slower                                                       |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.06x slower                                                        |
| sphinx                           | 409 ms                                                         | 436 ms: 1.07x slower                                                        |
| richards                         | 22.1 ms                                                        | 23.5 ms: 1.07x slower                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 343 ms: 1.07x slower                                                        |
| logging_simple                   | 2.24 us                                                        | 2.40 us: 1.07x slower                                                       |
| logging_format                   | 2.45 us                                                        | 2.63 us: 1.08x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 51.8 ms: 1.08x slower                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.08x slower                                                        |
| shortest_path                    | 225 ms                                                         | 245 ms: 1.09x slower                                                        |
| pprint_pformat                   | 650 ms                                                         | 709 ms: 1.09x slower                                                        |
| hexiom                           | 2.85 ms                                                        | 3.12 ms: 1.09x slower                                                       |
| thrift                           | 309 us                                                         | 338 us: 1.10x slower                                                        |
| richards_super                   | 24.7 ms                                                        | 27.1 ms: 1.10x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 11.8 ms: 1.10x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 41.6 ms: 1.10x slower                                                       |
| spectral_norm                    | 43.7 ms                                                        | 48.5 ms: 1.11x slower                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.3 ms: 1.11x slower                                                       |
| 2to3                             | 112 ms                                                         | 124 ms: 1.11x slower                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 48.8 ms: 1.13x slower                                                       |
| nqueens                          | 37.2 ms                                                        | 42.1 ms: 1.13x slower                                                       |
| xml_etree_process                | 25.4 ms                                                        | 28.8 ms: 1.14x slower                                                       |
| bench_thread_pool                | 412 us                                                         | 469 us: 1.14x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                        |
| connected_components             | 208 ms                                                         | 237 ms: 1.14x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 59.7 ms: 1.14x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.80 ms: 1.14x slower                                                       |
| chaos                            | 24.3 ms                                                        | 28.3 ms: 1.16x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 186 ms: 1.17x slower                                                        |
| comprehensions                   | 6.80 us                                                        | 8.07 us: 1.19x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 155 us: 1.19x slower                                                        |
| logging_silent                   | 40.6 ns                                                        | 48.9 ns: 1.20x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 40.7 ms: 1.21x slower                                                       |
| deltablue                        | 1.45 ms                                                        | 1.77 ms: 1.22x slower                                                       |
| mako                             | 4.41 ms                                                        | 5.40 ms: 1.22x slower                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.18 ms: 1.22x slower                                                       |
| many_optionals                   | 200 us                                                         | 246 us: 1.23x slower                                                        |
| raytrace                         | 109 ms                                                         | 134 ms: 1.23x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 263 ms: 1.26x slower                                                        |
| coverage                         | 31.2 ms                                                        | 40.3 ms: 1.29x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 62.5 ms: 1.30x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                       |
| nbody                            | 42.5 ms                                                        | 58.3 ms: 1.37x slower                                                       |
| generators                       | 15.7 ms                                                        | 22.7 ms: 1.44x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 63.4 ms: 1.48x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 161 ms: 1.57x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 108 ms: 3.74x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                                |

Benchmark hidden because not significant (3): async_tree_memoization, async_tree_cpu_io_mixed, async_tree_none_tg
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261031-3.16.0a1+dev-410fdda-NOGIL/bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.010x faster

# HPT report

- Reliability score: 73.08% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.23x