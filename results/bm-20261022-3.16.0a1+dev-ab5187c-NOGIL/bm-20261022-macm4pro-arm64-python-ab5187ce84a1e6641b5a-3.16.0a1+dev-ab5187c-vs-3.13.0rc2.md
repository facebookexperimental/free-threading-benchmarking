# Results vs. 3.13.0rc2

- fork: python
- ref: ab5187ce84a1e6641b5a
- machine: darwin-arm64
- commit hash: ab5187c
- commit date: 2026-10-22
- overall geometric mean: 1.006x slower
- HPT reliability: 82.50%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 126 ms: 1.13x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                      |
| html5lib       | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                       |
| sphinx         | 409 ms                                                         | 440 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                          | 1.04x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 287 ms: 1.81x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 290 ms: 1.81x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 289 ms: 1.40x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 298 ms: 1.29x faster                                                        |
| async_generators                 | 193 ms                                                         | 157 ms: 1.23x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 178 ms: 1.04x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 289 ms: 1.04x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 124 ms: 1.02x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 137 ms: 1.03x slower                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 48.4 ms: 1.12x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 12.7 ms: 1.18x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 270 ms: 1.30x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 161 ms: 1.57x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 111 ms: 3.85x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                                |

Benchmark hidden because not significant (3): async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                        |
| float          | 31.4 ms                                                        | 32.5 ms: 1.04x slower                                                       |
| nbody          | 42.5 ms                                                        | 58.9 ms: 1.39x slower                                                       |
| Geometric mean | (ref)                                                          | 1.11x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.33 ms: 1.22x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.07 ms: 1.18x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 89.4 ms: 1.06x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 63.2 ms: 1.32x slower                                                       |
| Geometric mean | (ref)                                                          | 1.04x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.86 ms: 1.21x faster                                                       |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.6 ms: 1.13x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 881 ms: 1.13x faster                                                        |
| xml_etree_parse      | 62.4 ms                                                        | 57.9 ms: 1.08x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 107 us: 1.08x slower                                                        |
| xml_etree_generate   | 35.8 ms                                                        | 38.7 ms: 1.08x slower                                                       |
| xml_etree_process    | 25.4 ms                                                        | 29.4 ms: 1.16x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 159 us: 1.22x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.28 ms: 1.07x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 7.22 ms: 1.21x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.71 ms: 1.29x slower                                                       |
| django_template | 12.5 ms                                                        | 17.2 ms: 1.38x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.33x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 758 us: 2.69x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 456 us: 2.18x faster                                                        |
| pylint                           | 106 ms                                                         | 52.4 ms: 2.02x faster                                                       |
| mdp                              | 1.06 sec                                                       | 579 ms: 1.83x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 287 ms: 1.81x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 290 ms: 1.81x faster                                                        |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.47x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.28 ms: 1.46x faster                                                       |
| async_tree_io_tg                 | 405 ms                                                         | 289 ms: 1.40x faster                                                        |
| deepcopy                         | 145 us                                                         | 107 us: 1.35x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 298 ms: 1.29x faster                                                        |
| async_generators                 | 193 ms                                                         | 157 ms: 1.23x faster                                                        |
| go                               | 72.6 ms                                                        | 59.6 ms: 1.22x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.33 ms: 1.22x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.86 ms: 1.21x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 790 ns: 1.20x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.07 ms: 1.18x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 14.0 us: 1.18x faster                                                       |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.6 ms: 1.13x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 881 ms: 1.13x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 57.2 us: 1.13x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 57.6 ms: 1.11x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                      |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 57.9 ms: 1.08x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 89.4 ms: 1.06x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 178 ms: 1.04x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                       |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 289 ms: 1.04x faster                                                        |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                       |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                       |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                      |
| telco                            | 3.07 ms                                                        | 3.10 ms: 1.01x slower                                                       |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 124 ms: 1.02x slower                                                        |
| scimark_fft                      | 124 ms                                                         | 127 ms: 1.02x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 137 ms: 1.03x slower                                                        |
| float                            | 31.4 ms                                                        | 32.5 ms: 1.04x slower                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 8.01 ms: 1.06x slower                                                       |
| python_startup                   | 8.63 ms                                                        | 9.28 ms: 1.07x slower                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 107 us: 1.08x slower                                                        |
| sphinx                           | 409 ms                                                         | 440 ms: 1.08x slower                                                        |
| richards                         | 22.1 ms                                                        | 23.9 ms: 1.08x slower                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 38.7 ms: 1.08x slower                                                       |
| logging_simple                   | 2.24 us                                                        | 2.42 us: 1.08x slower                                                       |
| logging_format                   | 2.45 us                                                        | 2.66 us: 1.09x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 52.2 ms: 1.09x slower                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 351 ms: 1.09x slower                                                        |
| shortest_path                    | 225 ms                                                         | 246 ms: 1.09x slower                                                        |
| hexiom                           | 2.85 ms                                                        | 3.11 ms: 1.09x slower                                                       |
| richards_super                   | 24.7 ms                                                        | 27.3 ms: 1.11x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 42.2 ms: 1.12x slower                                                       |
| thrift                           | 309 us                                                         | 345 us: 1.12x slower                                                        |
| pprint_pformat                   | 650 ms                                                         | 728 ms: 1.12x slower                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 48.4 ms: 1.12x slower                                                       |
| spectral_norm                    | 43.7 ms                                                        | 49.2 ms: 1.12x slower                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.7 ms: 1.13x slower                                                       |
| 2to3                             | 112 ms                                                         | 126 ms: 1.13x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                        |
| connected_components             | 208 ms                                                         | 239 ms: 1.15x slower                                                        |
| nqueens                          | 37.2 ms                                                        | 42.9 ms: 1.15x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 60.4 ms: 1.16x slower                                                       |
| xml_etree_process                | 25.4 ms                                                        | 29.4 ms: 1.16x slower                                                       |
| chaos                            | 24.3 ms                                                        | 28.3 ms: 1.16x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 186 ms: 1.17x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 12.7 ms: 1.18x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 48.5 ns: 1.20x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 40.5 ms: 1.20x slower                                                       |
| comprehensions                   | 6.80 us                                                        | 8.25 us: 1.21x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 7.22 ms: 1.21x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 159 us: 1.22x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.17 ms: 1.22x slower                                                       |
| deltablue                        | 1.45 ms                                                        | 1.77 ms: 1.22x slower                                                       |
| raytrace                         | 109 ms                                                         | 134 ms: 1.23x slower                                                        |
| many_optionals                   | 200 us                                                         | 252 us: 1.26x slower                                                        |
| mako                             | 4.41 ms                                                        | 5.71 ms: 1.29x slower                                                       |
| coverage                         | 31.2 ms                                                        | 40.5 ms: 1.30x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 270 ms: 1.30x slower                                                        |
| regex_compile                    | 47.9 ms                                                        | 63.2 ms: 1.32x slower                                                       |
| django_template                  | 12.5 ms                                                        | 17.2 ms: 1.38x slower                                                       |
| nbody                            | 42.5 ms                                                        | 58.9 ms: 1.39x slower                                                       |
| bench_thread_pool                | 412 us                                                         | 577 us: 1.40x slower                                                        |
| generators                       | 15.7 ms                                                        | 23.1 ms: 1.47x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 65.1 ms: 1.52x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 161 ms: 1.57x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 111 ms: 3.85x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                                |

Benchmark hidden because not significant (5): async_tree_none, async_tree_memoization, json_loads, pycparser, async_tree_cpu_io_mixed
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261022-3.16.0a1+dev-ab5187c-NOGIL/bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 82.50% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.26x