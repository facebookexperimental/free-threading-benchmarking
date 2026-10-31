# Results vs. 3.13.0rc2

- fork: python
- ref: 4a9b98115fec4d93c32c
- machine: darwin-arm64
- commit hash: 4a9b981
- commit date: 2026-10-30
- overall geometric mean: 1.011x faster
- HPT reliability: 63.11%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                      |
| html5lib       | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                       |
| sphinx         | 409 ms                                                         | 436 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                          | 1.02x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 284 ms: 1.85x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 283 ms: 1.84x faster                                                        |
| async_generators                 | 193 ms                                                         | 109 ms: 1.77x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 286 ms: 1.42x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 291 ms: 1.33x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 180 ms: 1.08x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 134 ms: 1.07x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 176 ms: 1.06x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 286 ms: 1.06x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 178 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 48.1 ms: 1.11x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 12.0 ms: 1.12x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 261 ms: 1.25x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 159 ms: 1.55x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 109 ms: 3.76x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                                |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed, async_tree_eager_memoization, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 157 ms: 1.05x faster                                                        |
| float          | 31.4 ms                                                        | 32.2 ms: 1.03x slower                                                       |
| nbody          | 42.5 ms                                                        | 58.9 ms: 1.38x slower                                                       |
| Geometric mean | (ref)                                                          | 1.10x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.30 ms: 1.24x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 8.98 ms: 1.19x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 88.7 ms: 1.07x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 62.7 ms: 1.31x slower                                                       |
| Geometric mean | (ref)                                                          | 1.05x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.64 ms: 1.28x faster                                                       |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.3 ms: 1.17x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 876 ms: 1.14x faster                                                        |
| xml_etree_parse      | 62.4 ms                                                        | 57.0 ms: 1.09x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 38.3 ms: 1.07x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 107 us: 1.08x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.1 ms: 1.15x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 156 us: 1.19x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.92 ms: 1.03x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.85 ms: 1.15x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.09x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.66 ms: 1.28x slower                                                       |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.31x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 761 us: 2.68x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 461 us: 2.16x faster                                                        |
| pylint                           | 106 ms                                                         | 51.4 ms: 2.06x faster                                                       |
| mdp                              | 1.06 sec                                                       | 567 ms: 1.87x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 284 ms: 1.85x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 283 ms: 1.84x faster                                                        |
| async_generators                 | 193 ms                                                         | 109 ms: 1.77x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.19 ms: 1.49x faster                                                       |
| k_core                           | 1.46 sec                                                       | 996 ms: 1.47x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 286 ms: 1.42x faster                                                        |
| deepcopy                         | 145 us                                                         | 107 us: 1.35x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 291 ms: 1.33x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.64 ms: 1.28x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.30 ms: 1.24x faster                                                       |
| go                               | 72.6 ms                                                        | 59.1 ms: 1.23x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 13.5 us: 1.22x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 53.2 us: 1.22x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 8.98 ms: 1.19x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.3 ms: 1.17x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 823 ns: 1.15x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 876 ms: 1.14x faster                                                        |
| scimark_sor                      | 64.0 ms                                                        | 56.8 ms: 1.13x faster                                                       |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.12x faster                                                      |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 57.0 ms: 1.09x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 180 ms: 1.08x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 88.7 ms: 1.07x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 134 ms: 1.07x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 176 ms: 1.06x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 286 ms: 1.06x faster                                                        |
| pidigits                         | 166 ms                                                         | 157 ms: 1.05x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                       |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                      |
| async_tree_memoization           | 184 ms                                                         | 178 ms: 1.04x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                       |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                       |
| telco                            | 3.07 ms                                                        | 3.04 ms: 1.01x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                        |
| float                            | 31.4 ms                                                        | 32.2 ms: 1.03x slower                                                       |
| python_startup                   | 8.63 ms                                                        | 8.92 ms: 1.03x slower                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.93 ms: 1.05x slower                                                       |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                        |
| sphinx                           | 409 ms                                                         | 436 ms: 1.07x slower                                                        |
| logging_format                   | 2.45 us                                                        | 2.61 us: 1.07x slower                                                       |
| logging_simple                   | 2.24 us                                                        | 2.39 us: 1.07x slower                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 38.3 ms: 1.07x slower                                                       |
| richards                         | 22.1 ms                                                        | 23.7 ms: 1.07x slower                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 346 ms: 1.07x slower                                                        |
| unpickle_pure_python             | 99.5 us                                                        | 107 us: 1.08x slower                                                        |
| hexiom                           | 2.85 ms                                                        | 3.08 ms: 1.08x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 41.2 ms: 1.09x slower                                                       |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                        |
| shortest_path                    | 225 ms                                                         | 246 ms: 1.09x slower                                                        |
| richards_super                   | 24.7 ms                                                        | 27.1 ms: 1.10x slower                                                       |
| thrift                           | 309 us                                                         | 341 us: 1.10x slower                                                        |
| pprint_pformat                   | 650 ms                                                         | 718 ms: 1.11x slower                                                        |
| meteor_contest                   | 47.9 ms                                                        | 53.0 ms: 1.11x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 48.1 ms: 1.11x slower                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.3 ms: 1.12x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 12.0 ms: 1.12x slower                                                       |
| nqueens                          | 37.2 ms                                                        | 41.7 ms: 1.12x slower                                                       |
| spectral_norm                    | 43.7 ms                                                        | 49.4 ms: 1.13x slower                                                       |
| bench_thread_pool                | 412 us                                                         | 467 us: 1.13x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 59.9 ms: 1.15x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.15x slower                                                        |
| connected_components             | 208 ms                                                         | 239 ms: 1.15x slower                                                        |
| xml_etree_process                | 25.4 ms                                                        | 29.1 ms: 1.15x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.85 ms: 1.15x slower                                                       |
| chaos                            | 24.3 ms                                                        | 28.1 ms: 1.16x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.18x slower                                                        |
| comprehensions                   | 6.80 us                                                        | 8.03 us: 1.18x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 156 us: 1.19x slower                                                        |
| deltablue                        | 1.45 ms                                                        | 1.74 ms: 1.20x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 40.4 ms: 1.20x slower                                                       |
| many_optionals                   | 200 us                                                         | 242 us: 1.21x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.16 ms: 1.21x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 49.3 ns: 1.21x slower                                                       |
| raytrace                         | 109 ms                                                         | 134 ms: 1.24x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 261 ms: 1.25x slower                                                        |
| mako                             | 4.41 ms                                                        | 5.66 ms: 1.28x slower                                                       |
| coverage                         | 31.2 ms                                                        | 40.1 ms: 1.29x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 62.7 ms: 1.31x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                       |
| nbody                            | 42.5 ms                                                        | 58.9 ms: 1.38x slower                                                       |
| generators                       | 15.7 ms                                                        | 22.6 ms: 1.44x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 64.2 ms: 1.50x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 159 ms: 1.55x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 109 ms: 3.76x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                                |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed, json_loads, fannkuch, pycparser, async_tree_eager_memoization, async_tree_none_tg
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261030-3.16.0a1+dev-4a9b981-NOGIL/bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 63.11% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.23x