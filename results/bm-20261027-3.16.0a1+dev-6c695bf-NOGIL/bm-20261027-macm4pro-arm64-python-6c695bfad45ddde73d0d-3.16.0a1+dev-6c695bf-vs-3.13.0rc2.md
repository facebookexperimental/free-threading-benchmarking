# Results vs. 3.13.0rc2

- fork: python
- ref: 6c695bfad45ddde73d0d
- machine: darwin-arm64
- commit hash: 6c695bf
- commit date: 2026-10-27
- overall geometric mean: 1.002x slower
- HPT reliability: 78.88%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                      |
| html5lib       | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                       |
| sphinx         | 409 ms                                                         | 441 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                          | 1.04x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 290 ms: 1.79x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 293 ms: 1.79x faster                                                        |
| async_generators                 | 193 ms                                                         | 112 ms: 1.72x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 292 ms: 1.39x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 304 ms: 1.27x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.06x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 179 ms: 1.04x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 137 ms: 1.04x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 293 ms: 1.03x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 180 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 138 ms: 1.04x slower                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 49.3 ms: 1.14x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 12.4 ms: 1.16x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 268 ms: 1.29x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 162 ms: 1.57x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 110 ms: 3.79x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                                |

Benchmark hidden because not significant (2): async_tree_eager_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 159 ms: 1.05x faster                                                        |
| float          | 31.4 ms                                                        | 32.5 ms: 1.03x slower                                                       |
| nbody          | 42.5 ms                                                        | 59.2 ms: 1.39x slower                                                       |
| Geometric mean | (ref)                                                          | 1.11x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.32 ms: 1.23x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.01 ms: 1.19x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 88.8 ms: 1.07x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 63.3 ms: 1.32x slower                                                       |
| Geometric mean | (ref)                                                          | 1.04x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.68 ms: 1.27x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 867 ms: 1.15x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.3 ms: 1.15x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 58.3 ms: 1.07x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 38.5 ms: 1.08x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.09x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.6 ms: 1.17x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 157 us: 1.20x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.80 ms: 1.02x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.81 ms: 1.14x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                       |
| django_template | 12.5 ms                                                        | 16.9 ms: 1.35x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.31x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 752 us: 2.72x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 460 us: 2.16x faster                                                        |
| pylint                           | 106 ms                                                         | 51.0 ms: 2.07x faster                                                       |
| mdp                              | 1.06 sec                                                       | 583 ms: 1.82x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 290 ms: 1.79x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 293 ms: 1.79x faster                                                        |
| async_generators                 | 193 ms                                                         | 112 ms: 1.72x faster                                                        |
| k_core                           | 1.46 sec                                                       | 993 ms: 1.47x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.32 ms: 1.45x faster                                                       |
| async_tree_io_tg                 | 405 ms                                                         | 292 ms: 1.39x faster                                                        |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 304 ms: 1.27x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.68 ms: 1.27x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.32 ms: 1.23x faster                                                       |
| go                               | 72.6 ms                                                        | 59.6 ms: 1.22x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 53.9 us: 1.20x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 9.01 ms: 1.19x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 13.9 us: 1.18x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 818 ns: 1.16x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 867 ms: 1.15x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.3 ms: 1.15x faster                                                       |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                        |
| scimark_sor                      | 64.0 ms                                                        | 57.5 ms: 1.11x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.11x faster                                                      |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 58.3 ms: 1.07x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 88.8 ms: 1.07x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.06x faster                                                        |
| pidigits                         | 166 ms                                                         | 159 ms: 1.05x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.05x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 179 ms: 1.04x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 137 ms: 1.04x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 293 ms: 1.03x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 180 ms: 1.02x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                       |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                       |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                      |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                        |
| telco                            | 3.07 ms                                                        | 3.09 ms: 1.01x slower                                                       |
| python_startup                   | 8.63 ms                                                        | 8.80 ms: 1.02x slower                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                                        |
| float                            | 31.4 ms                                                        | 32.5 ms: 1.03x slower                                                       |
| async_tree_none_tg               | 133 ms                                                         | 138 ms: 1.04x slower                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 8.04 ms: 1.07x slower                                                       |
| scimark_fft                      | 124 ms                                                         | 133 ms: 1.07x slower                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 38.5 ms: 1.08x slower                                                       |
| sphinx                           | 409 ms                                                         | 441 ms: 1.08x slower                                                        |
| richards                         | 22.1 ms                                                        | 23.9 ms: 1.08x slower                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.09x slower                                                        |
| pprint_safe_repr                 | 322 ms                                                         | 352 ms: 1.09x slower                                                        |
| logging_simple                   | 2.24 us                                                        | 2.47 us: 1.10x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                       |
| richards_super                   | 24.7 ms                                                        | 27.3 ms: 1.11x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 41.9 ms: 1.11x slower                                                       |
| logging_format                   | 2.45 us                                                        | 2.71 us: 1.11x slower                                                       |
| shortest_path                    | 225 ms                                                         | 250 ms: 1.11x slower                                                        |
| hexiom                           | 2.85 ms                                                        | 3.17 ms: 1.11x slower                                                       |
| pprint_pformat                   | 650 ms                                                         | 726 ms: 1.12x slower                                                        |
| thrift                           | 309 us                                                         | 346 us: 1.12x slower                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.5 ms: 1.12x slower                                                       |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                        |
| nqueens                          | 37.2 ms                                                        | 42.2 ms: 1.13x slower                                                       |
| bench_thread_pool                | 412 us                                                         | 467 us: 1.13x slower                                                        |
| spectral_norm                    | 43.7 ms                                                        | 49.9 ms: 1.14x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 49.3 ms: 1.14x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.81 ms: 1.14x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.16x slower                                                        |
| connected_components             | 208 ms                                                         | 240 ms: 1.16x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 12.4 ms: 1.16x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 60.6 ms: 1.16x slower                                                       |
| xml_etree_process                | 25.4 ms                                                        | 29.6 ms: 1.17x slower                                                       |
| chaos                            | 24.3 ms                                                        | 28.5 ms: 1.17x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.18x slower                                                        |
| comprehensions                   | 6.80 us                                                        | 8.09 us: 1.19x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 157 us: 1.20x slower                                                        |
| deltablue                        | 1.45 ms                                                        | 1.77 ms: 1.22x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 41.2 ms: 1.22x slower                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.19 ms: 1.23x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 50.0 ns: 1.23x slower                                                       |
| raytrace                         | 109 ms                                                         | 135 ms: 1.24x slower                                                        |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                        |
| mako                             | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 268 ms: 1.29x slower                                                        |
| coverage                         | 31.2 ms                                                        | 40.8 ms: 1.31x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 63.3 ms: 1.32x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.9 ms: 1.35x slower                                                       |
| nbody                            | 42.5 ms                                                        | 59.2 ms: 1.39x slower                                                       |
| generators                       | 15.7 ms                                                        | 23.1 ms: 1.47x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 65.8 ms: 1.54x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 162 ms: 1.57x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 110 ms: 3.79x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                                |

Benchmark hidden because not significant (4): pycparser, json_loads, async_tree_eager_memoization, async_tree_cpu_io_mixed
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261027-3.16.0a1+dev-6c695bf-NOGIL/bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 78.88% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x