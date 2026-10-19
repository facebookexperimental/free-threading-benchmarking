# Results vs. 3.13.0rc2

- fork: python
- ref: 010bebbf9fd12bba1e3f
- machine: darwin-arm64
- commit hash: 010bebb
- commit date: 2026-10-16
- overall geometric mean: 1.045x faster
- HPT reliability: 69.50%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.09x slower                                                        |
| docutils       | 1.05 sec                                                       | 997 ms: 1.05x faster                                                        |
| html5lib       | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                       |
| sphinx         | 409 ms                                                         | 422 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                          | 1.00x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 278 ms: 1.89x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 277 ms: 1.88x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 277 ms: 1.46x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 277 ms: 1.40x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.08x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 133 ms: 1.07x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 285 ms: 1.06x faster                                                        |
| async_generators                 | 193 ms                                                         | 183 ms: 1.05x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 177 ms: 1.04x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 119 ms: 1.03x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 45.2 ms: 1.05x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 267 ms: 1.28x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 157 ms: 1.53x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 107 ms: 3.68x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                                |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                        |
| float          | 31.4 ms                                                        | 30.6 ms: 1.03x faster                                                       |
| nbody          | 42.5 ms                                                        | 53.3 ms: 1.25x slower                                                       |
| Geometric mean | (ref)                                                          | 1.05x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 8.86 ms: 1.21x faster                                                       |
| regex_effbot   | 1.61 ms                                                        | 1.34 ms: 1.20x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 87.6 ms: 1.08x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 58.6 ms: 1.22x slower                                                       |
| Geometric mean | (ref)                                                          | 1.06x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.64 ms: 1.28x faster                                                       |
| xml_etree_iterparse  | 46.1 ms                                                        | 37.3 ms: 1.24x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 832 ms: 1.20x faster                                                        |
| xml_etree_parse      | 62.4 ms                                                        | 56.9 ms: 1.10x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 96.1 us: 1.03x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 26.6 ms: 1.05x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.11x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.76 ms: 1.13x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 7.16 ms: 1.20x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                       |
| mako            | 4.41 ms                                                        | 5.59 ms: 1.27x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.26x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 760 us: 2.68x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 459 us: 2.17x faster                                                        |
| pylint                           | 106 ms                                                         | 50.5 ms: 2.09x faster                                                       |
| mdp                              | 1.06 sec                                                       | 551 ms: 1.92x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 278 ms: 1.89x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 277 ms: 1.88x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.02 ms: 1.56x faster                                                       |
| k_core                           | 1.46 sec                                                       | 964 ms: 1.52x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 277 ms: 1.46x faster                                                        |
| deepcopy                         | 145 us                                                         | 100.0 us: 1.45x faster                                                      |
| async_tree_io                    | 386 ms                                                         | 277 ms: 1.40x faster                                                        |
| go                               | 72.6 ms                                                        | 55.2 ms: 1.31x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.64 ms: 1.28x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.3 ms: 1.24x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 13.4 us: 1.23x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 52.6 ms: 1.22x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 8.86 ms: 1.21x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 785 ns: 1.21x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 53.6 us: 1.21x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 832 ms: 1.20x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.34 ms: 1.20x faster                                                       |
| pyflate                          | 222 ms                                                         | 187 ms: 1.19x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.09 us: 1.19x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.89 sec: 1.13x faster                                                      |
| xml_etree_parse                  | 62.4 ms                                                        | 56.9 ms: 1.10x faster                                                       |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 87.6 ms: 1.08x faster                                                       |
| html5lib                         | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.08x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 133 ms: 1.07x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 285 ms: 1.06x faster                                                        |
| async_generators                 | 193 ms                                                         | 183 ms: 1.05x faster                                                        |
| docutils                         | 1.05 sec                                                       | 997 ms: 1.05x faster                                                        |
| pycparser                        | 470 ms                                                         | 450 ms: 1.05x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 177 ms: 1.04x faster                                                        |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                        |
| json                             | 1.94 ms                                                        | 1.87 ms: 1.04x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 96.1 us: 1.03x faster                                                       |
| float                            | 31.4 ms                                                        | 30.6 ms: 1.03x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 119 ms: 1.03x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                       |
| generators                       | 15.7 ms                                                        | 15.4 ms: 1.02x faster                                                       |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 43.9 ms: 1.00x slower                                                       |
| richards                         | 22.1 ms                                                        | 22.2 ms: 1.00x slower                                                       |
| telco                            | 3.07 ms                                                        | 3.09 ms: 1.01x slower                                                       |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                        |
| hexiom                           | 2.85 ms                                                        | 2.88 ms: 1.01x slower                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                        |
| nqueens                          | 37.2 ms                                                        | 37.8 ms: 1.02x slower                                                       |
| logging_format                   | 2.45 us                                                        | 2.49 us: 1.02x slower                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.68 ms: 1.02x slower                                                       |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.02x slower                                                        |
| pprint_safe_repr                 | 322 ms                                                         | 330 ms: 1.02x slower                                                        |
| logging_simple                   | 2.24 us                                                        | 2.29 us: 1.02x slower                                                       |
| richards_super                   | 24.7 ms                                                        | 25.3 ms: 1.02x slower                                                       |
| sphinx                           | 409 ms                                                         | 422 ms: 1.03x slower                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 45.2 ms: 1.05x slower                                                       |
| thrift                           | 309 us                                                         | 324 us: 1.05x slower                                                        |
| xml_etree_process                | 25.4 ms                                                        | 26.6 ms: 1.05x slower                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 31.6 ms: 1.06x slower                                                       |
| pprint_pformat                   | 650 ms                                                         | 690 ms: 1.06x slower                                                        |
| logging_silent                   | 40.6 ns                                                        | 43.1 ns: 1.06x slower                                                       |
| 2to3                             | 112 ms                                                         | 121 ms: 1.09x slower                                                        |
| comprehensions                   | 6.80 us                                                        | 7.39 us: 1.09x slower                                                       |
| deltablue                        | 1.45 ms                                                        | 1.59 ms: 1.09x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 105 ms: 1.10x slower                                                        |
| shortest_path                    | 225 ms                                                         | 247 ms: 1.10x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 57.6 ms: 1.10x slower                                                       |
| raytrace                         | 109 ms                                                         | 120 ms: 1.10x slower                                                        |
| chaos                            | 24.3 ms                                                        | 26.8 ms: 1.10x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 53.0 ms: 1.11x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 42.0 ms: 1.11x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 177 ms: 1.11x slower                                                        |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                        |
| python_startup                   | 8.63 ms                                                        | 9.76 ms: 1.13x slower                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.06 ms: 1.16x slower                                                       |
| connected_components             | 208 ms                                                         | 242 ms: 1.16x slower                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 40.4 ms: 1.20x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 7.16 ms: 1.20x slower                                                       |
| many_optionals                   | 200 us                                                         | 241 us: 1.20x slower                                                        |
| regex_compile                    | 47.9 ms                                                        | 58.6 ms: 1.22x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 52.9 ms: 1.24x slower                                                       |
| coverage                         | 31.2 ms                                                        | 39.0 ms: 1.25x slower                                                       |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                       |
| nbody                            | 42.5 ms                                                        | 53.3 ms: 1.25x slower                                                       |
| mako                             | 4.41 ms                                                        | 5.59 ms: 1.27x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 267 ms: 1.28x slower                                                        |
| bench_thread_pool                | 412 us                                                         | 573 us: 1.39x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 157 ms: 1.53x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 107 ms: 3.68x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                                |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, async_tree_none_tg
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261016-3.16.0a1+dev-010bebb-CLANG,NOGIL/bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.045x faster

# HPT report

- Reliability score: 69.50% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.25x