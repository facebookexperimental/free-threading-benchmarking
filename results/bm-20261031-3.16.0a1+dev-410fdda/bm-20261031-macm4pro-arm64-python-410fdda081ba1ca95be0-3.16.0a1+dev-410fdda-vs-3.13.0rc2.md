# Results vs. 3.13.0rc2

- fork: python
- ref: 410fdda081ba1ca95be0
- machine: darwin-arm64
- commit hash: 410fdda
- commit date: 2026-10-31
- overall geometric mean: 1.123x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.01x slower                                                        |
| docutils       | 1.05 sec                                                       | 885 ms: 1.18x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.1 ms: 1.15x faster                                                       |
| sphinx         | 409 ms                                                         | 381 ms: 1.07x faster                                                        |
| Geometric mean | (ref)                                                          | 1.10x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 262 ms: 2.01x faster                                                        |
| async_generators                 | 193 ms                                                         | 98.2 ms: 1.97x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 276 ms: 1.88x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 274 ms: 1.48x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 267 ms: 1.45x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.32x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.21x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 155 ms: 1.20x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 159 ms: 1.16x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.59 ms: 1.12x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.1 ms: 1.08x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 140 ms: 1.36x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.8 ms: 3.17x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.0 ms: 1.17x faster                                                       |
| pidigits       | 166 ms                                                         | 158 ms: 1.05x faster                                                        |
| nbody          | 42.5 ms                                                        | 42.8 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.29 ms: 1.25x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 8.99 ms: 1.19x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 87.6 ms: 1.08x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                       |
| Geometric mean | (ref)                                                          | 1.10x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.53 ms: 1.32x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 785 ms: 1.27x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.6 ms: 1.14x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 89.9 us: 1.11x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.3 us: 1.06x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.6 ms: 1.04x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.5 ms: 1.03x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 62.7 ms: 1.00x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 136 us: 1.05x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.09x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.13 ms: 1.06x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.33 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.00x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.37 ms: 1.01x faster                                                       |
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pylint                           | 106 ms                                                         | 49.8 ms: 2.12x faster                                                       |
| mdp                              | 1.06 sec                                                       | 499 ms: 2.12x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 262 ms: 2.01x faster                                                        |
| async_generators                 | 193 ms                                                         | 98.2 ms: 1.97x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 276 ms: 1.88x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 610 us: 1.63x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.90 ms: 1.61x faster                                                       |
| deepcopy                         | 145 us                                                         | 93.7 us: 1.55x faster                                                       |
| k_core                           | 1.46 sec                                                       | 964 ms: 1.52x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 274 ms: 1.48x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 267 ms: 1.45x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.43x faster                                                       |
| go                               | 72.6 ms                                                        | 51.0 ms: 1.42x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 45.5 us: 1.42x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 47.7 ms: 1.34x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.53 ms: 1.32x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.32x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 785 ms: 1.27x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.29 ms: 1.25x faster                                                       |
| pyflate                          | 222 ms                                                         | 180 ms: 1.23x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.21x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 155 ms: 1.20x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 8.99 ms: 1.19x faster                                                       |
| gc_traversal                     | 2.04 ms                                                        | 1.72 ms: 1.19x faster                                                       |
| docutils                         | 1.05 sec                                                       | 885 ms: 1.18x faster                                                        |
| float                            | 31.4 ms                                                        | 27.0 ms: 1.17x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 159 ms: 1.16x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 20.1 ms: 1.15x faster                                                       |
| fannkuch                         | 179 ms                                                         | 157 ms: 1.14x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.6 ms: 1.14x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.5 ms: 1.13x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 17.6 ms: 1.13x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 9.59 ms: 1.12x faster                                                       |
| scimark_fft                      | 124 ms                                                         | 111 ms: 1.12x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.11x faster                                                      |
| unpickle_pure_python             | 99.5 us                                                        | 89.9 us: 1.11x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.58 ms: 1.10x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.78 ms: 1.10x faster                                                       |
| richards                         | 22.1 ms                                                        | 20.0 ms: 1.10x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                        |
| richards_super                   | 24.7 ms                                                        | 22.6 ms: 1.09x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.3 ms: 1.09x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 87.6 ms: 1.08x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 40.1 ms: 1.08x faster                                                       |
| sphinx                           | 409 ms                                                         | 381 ms: 1.07x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                       |
| json                             | 1.94 ms                                                        | 1.82 ms: 1.07x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.13 ms: 1.06x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 41.3 ms: 1.06x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 305 ms: 1.06x faster                                                        |
| json_loads                       | 10.8 us                                                        | 10.3 us: 1.06x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 901 ns: 1.05x faster                                                        |
| pprint_pformat                   | 650 ms                                                         | 619 ms: 1.05x faster                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 7.18 ms: 1.05x faster                                                       |
| pidigits                         | 166 ms                                                         | 158 ms: 1.05x faster                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.70 ms: 1.05x faster                                                       |
| comprehensions                   | 6.80 us                                                        | 6.51 us: 1.05x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                        |
| thrift                           | 309 us                                                         | 296 us: 1.04x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                        |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 34.6 ms: 1.04x faster                                                       |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 24.5 ms: 1.03x faster                                                       |
| pycparser                        | 470 ms                                                         | 459 ms: 1.02x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.42 ms: 1.02x faster                                                       |
| mako                             | 4.41 ms                                                        | 4.37 ms: 1.01x faster                                                       |
| meteor_contest                   | 47.9 ms                                                        | 47.5 ms: 1.01x faster                                                       |
| bench_thread_pool                | 412 us                                                         | 409 us: 1.01x faster                                                        |
| connected_components             | 208 ms                                                         | 209 ms: 1.00x slower                                                        |
| shortest_path                    | 225 ms                                                         | 225 ms: 1.00x slower                                                        |
| chaos                            | 24.3 ms                                                        | 24.4 ms: 1.00x slower                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 62.7 ms: 1.00x slower                                                       |
| 2to3                             | 112 ms                                                         | 112 ms: 1.01x slower                                                        |
| nbody                            | 42.5 ms                                                        | 42.8 ms: 1.01x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 97.2 ms: 1.02x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 41.3 ns: 1.02x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 53.5 ms: 1.02x slower                                                       |
| raytrace                         | 109 ms                                                         | 112 ms: 1.02x slower                                                        |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                        |
| pickle_pure_python               | 130 us                                                         | 136 us: 1.05x slower                                                        |
| scimark_lu                       | 42.8 ms                                                        | 45.0 ms: 1.05x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.33 ms: 1.06x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 36.0 ms: 1.07x slower                                                       |
| generators                       | 15.7 ms                                                        | 16.8 ms: 1.07x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                       |
| many_optionals                   | 200 us                                                         | 224 us: 1.12x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 42.3 ms: 1.12x slower                                                       |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 140 ms: 1.36x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.8 ms: 3.17x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                                |
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261031-3.16.0a1+dev-410fdda/bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.123x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.10x