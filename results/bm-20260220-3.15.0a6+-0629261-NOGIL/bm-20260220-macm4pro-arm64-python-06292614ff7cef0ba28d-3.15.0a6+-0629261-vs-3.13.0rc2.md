# Results vs. 3.13.0rc2

- fork: python
- ref: 06292614ff7cef0ba28d
- machine: darwin-arm64
- commit hash: 0629261
- commit date: 2026-02-20
- overall geometric mean: 1.019x faster
- HPT reliability: 58.23%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.0 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 420 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 245 ms: 2.13x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 236 ms: 1.71x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.6 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.3 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.7 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.2 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.8 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.8 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.91 ms: 1.19x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 870 ms: 1.15x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.2 ms: 1.07x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.87 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.19 ms: 1.21x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.6 ms: 1.06x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                    |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.24x slower                                                    |
| mako            | 4.41 ms                                                        | 5.52 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 810 us: 2.52x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 245 ms: 2.13x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 507 us: 1.96x faster                                                     |
| mdp                              | 1.06 sec                                                       | 610 ms: 1.73x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 236 ms: 1.71x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.17 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 987 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 106 us: 1.36x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.9 us: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| go                               | 72.6 ms                                                        | 59.7 ms: 1.22x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.21x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 785 ns: 1.21x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.91 ms: 1.19x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.1 ms: 1.16x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 870 ms: 1.15x faster                                                     |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| float                            | 31.4 ms                                                        | 28.7 ms: 1.10x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.2 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                     |
| pycparser                        | 470 ms                                                         | 463 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.8 ms: 1.01x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 23.0 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 323 ms: 1.00x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                     |
| dask                             | 525 ms                                                         | 530 ms: 1.01x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 662 ms: 1.02x slower                                                     |
| sphinx                           | 409 ms                                                         | 420 ms: 1.03x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.04x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.0 ms: 1.04x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.6 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.8 ms: 1.06x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.2 ms: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.3 ns: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.11 ms: 1.08x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.41 us: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.6 ms: 1.08x slower                                                    |
| thrift                           | 309 us                                                         | 334 us: 1.08x slower                                                     |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.6 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.09x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.68 us: 1.10x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 118 ms: 1.11x slower                                                     |
| chaos                            | 24.3 ms                                                        | 27.1 ms: 1.12x slower                                                    |
| shortest_path                    | 225 ms                                                         | 252 ms: 1.12x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 72.6 us: 1.12x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 49.7 ms: 1.14x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 42.4 ms: 1.14x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.87 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.1 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.9 ms: 1.16x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.17x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.18x slower                                                     |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.13 ms: 1.19x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.20 us: 1.21x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.19 ms: 1.21x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.24x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.9 ms: 1.24x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.9 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.52 ms: 1.25x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 55.3 ms: 1.29x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 43.7 ms: 1.30x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.9 ms: 1.33x slower                                                    |
| many_optionals                   | 200 us                                                         | 268 us: 1.34x slower                                                     |
| nbody                            | 42.5 ms                                                        | 57.2 ms: 1.34x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 577 us: 1.40x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.3 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (2): json, async_tree_eager_cpu_io_mixed
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260220-3.15.0a6+-0629261-NOGIL/bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.019x faster

# HPT report

- Reliability score: 58.23% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.32x