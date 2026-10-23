# Results vs. 3.13.0rc2

- fork: python
- ref: fd657b067473fdf549df
- machine: darwin-arm64
- commit hash: fd657b0
- commit date: 2026-10-23
- overall geometric mean: 1.116x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.02x slower                                                        |
| docutils       | 1.05 sec                                                       | 892 ms: 1.17x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.0 ms: 1.15x faster                                                       |
| sphinx         | 409 ms                                                         | 384 ms: 1.06x faster                                                        |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 261 ms: 2.02x faster                                                        |
| async_generators                 | 193 ms                                                         | 99.5 ms: 1.94x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 276 ms: 1.89x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 274 ms: 1.48x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 265 ms: 1.46x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.31x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.21x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 156 ms: 1.19x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 159 ms: 1.16x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 270 ms: 1.11x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.70 ms: 1.11x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.11x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 140 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.1 ms: 3.18x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                       |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                        |
| nbody          | 42.5 ms                                                        | 43.3 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                          | 1.06x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.29 ms: 1.25x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 8.97 ms: 1.19x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 87.4 ms: 1.08x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 53.6 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                          | 1.10x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.50 ms: 1.33x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 789 ms: 1.27x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.3 ms: 1.14x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 93.5 us: 1.06x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.2 us: 1.06x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.7 ms: 1.03x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 62.1 ms: 1.00x faster                                                       |
| pickle_pure_python   | 130 us                                                         | 138 us: 1.06x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.09x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.16 ms: 1.06x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.00x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                                |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 497 ms: 2.13x faster                                                        |
| pylint                           | 106 ms                                                         | 51.4 ms: 2.05x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 261 ms: 2.02x faster                                                        |
| async_generators                 | 193 ms                                                         | 99.5 ms: 1.94x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 276 ms: 1.89x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 613 us: 1.62x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.92 ms: 1.60x faster                                                       |
| deepcopy                         | 145 us                                                         | 95.0 us: 1.53x faster                                                       |
| k_core                           | 1.46 sec                                                       | 972 ms: 1.51x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 274 ms: 1.48x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 265 ms: 1.46x faster                                                        |
| go                               | 72.6 ms                                                        | 50.9 ms: 1.43x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 47.8 us: 1.35x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 48.0 ms: 1.33x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.50 ms: 1.33x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.31x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.02 us: 1.27x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 789 ms: 1.27x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.29 ms: 1.25x faster                                                       |
| pyflate                          | 222 ms                                                         | 180 ms: 1.23x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.21x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 8.97 ms: 1.19x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 156 ms: 1.19x faster                                                        |
| gc_traversal                     | 2.04 ms                                                        | 1.74 ms: 1.17x faster                                                       |
| docutils                         | 1.05 sec                                                       | 892 ms: 1.17x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 159 ms: 1.16x faster                                                        |
| float                            | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                       |
| html5lib                         | 23.1 ms                                                        | 20.0 ms: 1.15x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.3 ms: 1.14x faster                                                       |
| dulwich_log                      | 19.8 ms                                                        | 17.5 ms: 1.13x faster                                                       |
| fannkuch                         | 179 ms                                                         | 158 ms: 1.13x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.90 sec: 1.12x faster                                                      |
| richards                         | 22.1 ms                                                        | 19.8 ms: 1.11x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 270 ms: 1.11x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.8 ms: 1.11x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 9.70 ms: 1.11x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 22.3 ms: 1.11x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.11x faster                                                        |
| hexiom                           | 2.85 ms                                                        | 2.59 ms: 1.10x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                        |
| scimark_fft                      | 124 ms                                                         | 113 ms: 1.09x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 87.4 ms: 1.08x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.6 ms: 1.08x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.08 us: 1.07x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.86 ms: 1.07x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                       |
| logging_format                   | 2.45 us                                                        | 2.28 us: 1.07x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                       |
| json                             | 1.94 ms                                                        | 1.82 ms: 1.07x faster                                                       |
| sphinx                           | 409 ms                                                         | 384 ms: 1.06x faster                                                        |
| unpickle_pure_python             | 99.5 us                                                        | 93.5 us: 1.06x faster                                                       |
| json_loads                       | 10.8 us                                                        | 10.2 us: 1.06x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.16 ms: 1.06x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 41.6 ms: 1.05x faster                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.20 ms: 1.05x faster                                                       |
| comprehensions                   | 6.80 us                                                        | 6.53 us: 1.04x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 310 ms: 1.04x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 913 ns: 1.04x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                        |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 34.7 ms: 1.03x faster                                                       |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                        |
| pprint_pformat                   | 650 ms                                                         | 631 ms: 1.03x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.41 ms: 1.03x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.75 ms: 1.02x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                       |
| bench_thread_pool                | 412 us                                                         | 406 us: 1.01x faster                                                        |
| pycparser                        | 470 ms                                                         | 465 ms: 1.01x faster                                                        |
| logging_silent                   | 40.6 ns                                                        | 40.2 ns: 1.01x faster                                                       |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 62.1 ms: 1.00x faster                                                       |
| meteor_contest                   | 47.9 ms                                                        | 48.2 ms: 1.01x slower                                                       |
| chaos                            | 24.3 ms                                                        | 24.5 ms: 1.01x slower                                                       |
| 2to3                             | 112 ms                                                         | 113 ms: 1.02x slower                                                        |
| nbody                            | 42.5 ms                                                        | 43.3 ms: 1.02x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 97.5 ms: 1.02x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 53.9 ms: 1.03x slower                                                       |
| raytrace                         | 109 ms                                                         | 113 ms: 1.03x slower                                                        |
| sympy_expand                     | 159 ms                                                         | 165 ms: 1.04x slower                                                        |
| pickle_pure_python               | 130 us                                                         | 138 us: 1.06x slower                                                        |
| generators                       | 15.7 ms                                                        | 16.7 ms: 1.07x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 36.4 ms: 1.08x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 46.5 ms: 1.09x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 53.6 ms: 1.12x slower                                                       |
| many_optionals                   | 200 us                                                         | 225 us: 1.12x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 42.8 ms: 1.13x slower                                                       |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 140 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.1 ms: 3.18x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                                |

Benchmark hidden because not significant (2): shortest_path, mako
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261023-3.16.0a1+dev-fd657b0/bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.116x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.10x