# Results vs. 3.13.0rc2

- fork: python
- ref: fd657b067473fdf549df
- machine: darwin-arm64
- commit hash: fd657b0
- commit date: 2026-10-23
- overall geometric mean: 1.007x faster
- HPT reliability: 67.85%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                      |
| html5lib       | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                       |
| sphinx         | 409 ms                                                         | 436 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                          | 1.02x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 283 ms: 1.84x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 286 ms: 1.84x faster                                                        |
| async_generators                 | 193 ms                                                         | 111 ms: 1.74x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 288 ms: 1.41x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 290 ms: 1.33x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 180 ms: 1.07x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 285 ms: 1.06x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 135 ms: 1.06x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 177 ms: 1.05x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 178 ms: 1.04x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 48.2 ms: 1.12x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 12.1 ms: 1.13x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 261 ms: 1.25x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 160 ms: 1.56x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 108 ms: 3.73x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                                |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed, async_tree_eager_memoization, async_tree_eager_cpu_io_mixed, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 158 ms: 1.05x faster                                                        |
| float          | 31.4 ms                                                        | 32.7 ms: 1.04x slower                                                       |
| nbody          | 42.5 ms                                                        | 58.5 ms: 1.38x slower                                                       |
| Geometric mean | (ref)                                                          | 1.11x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.34 ms: 1.20x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 90.2 ms: 1.05x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 62.9 ms: 1.31x slower                                                       |
| Geometric mean | (ref)                                                          | 1.03x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 861 ms: 1.16x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.2 ms: 1.12x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 38.5 ms: 1.08x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.08x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.4 ms: 1.16x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 156 us: 1.20x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.81 ms: 1.02x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.83 ms: 1.15x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.70 ms: 1.29x slower                                                       |
| django_template | 12.5 ms                                                        | 16.8 ms: 1.35x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.32x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 755 us: 2.70x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 460 us: 2.16x faster                                                        |
| pylint                           | 106 ms                                                         | 51.9 ms: 2.04x faster                                                       |
| mdp                              | 1.06 sec                                                       | 572 ms: 1.85x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 283 ms: 1.84x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 286 ms: 1.84x faster                                                        |
| async_generators                 | 193 ms                                                         | 111 ms: 1.74x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.19 ms: 1.49x faster                                                       |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.48x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 288 ms: 1.41x faster                                                        |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 290 ms: 1.33x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                       |
| go                               | 72.6 ms                                                        | 59.4 ms: 1.22x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.34 ms: 1.20x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 792 ns: 1.20x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 14.0 us: 1.18x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 861 ms: 1.16x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 56.4 us: 1.15x faster                                                       |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.2 ms: 1.12x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.11x faster                                                      |
| scimark_sor                      | 64.0 ms                                                        | 57.6 ms: 1.11x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 180 ms: 1.07x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 285 ms: 1.06x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 135 ms: 1.06x faster                                                        |
| pidigits                         | 166 ms                                                         | 158 ms: 1.05x faster                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 177 ms: 1.05x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 90.2 ms: 1.05x faster                                                       |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.05x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 178 ms: 1.04x faster                                                        |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                       |
| html5lib                         | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                       |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                      |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                       |
| pycparser                        | 470 ms                                                         | 467 ms: 1.01x faster                                                        |
| telco                            | 3.07 ms                                                        | 3.08 ms: 1.01x slower                                                       |
| python_startup                   | 8.63 ms                                                        | 8.81 ms: 1.02x slower                                                       |
| float                            | 31.4 ms                                                        | 32.7 ms: 1.04x slower                                                       |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.04x slower                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 7.93 ms: 1.05x slower                                                       |
| sphinx                           | 409 ms                                                         | 436 ms: 1.07x slower                                                        |
| pprint_safe_repr                 | 322 ms                                                         | 345 ms: 1.07x slower                                                        |
| richards                         | 22.1 ms                                                        | 23.7 ms: 1.07x slower                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 38.5 ms: 1.08x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 51.8 ms: 1.08x slower                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.08x slower                                                        |
| hexiom                           | 2.85 ms                                                        | 3.11 ms: 1.09x slower                                                       |
| pprint_pformat                   | 650 ms                                                         | 710 ms: 1.09x slower                                                        |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                        |
| richards_super                   | 24.7 ms                                                        | 27.1 ms: 1.10x slower                                                       |
| logging_format                   | 2.45 us                                                        | 2.69 us: 1.10x slower                                                       |
| logging_simple                   | 2.24 us                                                        | 2.46 us: 1.10x slower                                                       |
| shortest_path                    | 225 ms                                                         | 249 ms: 1.11x slower                                                        |
| thrift                           | 309 us                                                         | 342 us: 1.11x slower                                                        |
| bench_thread_pool                | 412 us                                                         | 456 us: 1.11x slower                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 48.2 ms: 1.12x slower                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.5 ms: 1.12x slower                                                       |
| spectral_norm                    | 43.7 ms                                                        | 49.0 ms: 1.12x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 12.1 ms: 1.13x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 42.8 ms: 1.13x slower                                                       |
| nqueens                          | 37.2 ms                                                        | 42.3 ms: 1.14x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 59.5 ms: 1.14x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.83 ms: 1.15x slower                                                       |
| connected_components             | 208 ms                                                         | 239 ms: 1.15x slower                                                        |
| xml_etree_process                | 25.4 ms                                                        | 29.4 ms: 1.16x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 185 ms: 1.16x slower                                                        |
| chaos                            | 24.3 ms                                                        | 28.5 ms: 1.18x slower                                                       |
| comprehensions                   | 6.80 us                                                        | 8.04 us: 1.18x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 48.4 ns: 1.19x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 156 us: 1.20x slower                                                        |
| many_optionals                   | 200 us                                                         | 242 us: 1.21x slower                                                        |
| deltablue                        | 1.45 ms                                                        | 1.77 ms: 1.22x slower                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.17 ms: 1.22x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 41.3 ms: 1.23x slower                                                       |
| raytrace                         | 109 ms                                                         | 135 ms: 1.24x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 261 ms: 1.25x slower                                                        |
| mako                             | 4.41 ms                                                        | 5.70 ms: 1.29x slower                                                       |
| coverage                         | 31.2 ms                                                        | 40.4 ms: 1.30x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 62.9 ms: 1.31x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.8 ms: 1.35x slower                                                       |
| nbody                            | 42.5 ms                                                        | 58.5 ms: 1.38x slower                                                       |
| generators                       | 15.7 ms                                                        | 22.8 ms: 1.45x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 64.8 ms: 1.52x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 160 ms: 1.56x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 108 ms: 3.73x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                                |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed, async_tree_eager_memoization, fannkuch, async_tree_eager_cpu_io_mixed, async_tree_none_tg
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261023-3.16.0a1+dev-fd657b0-NOGIL/bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1+dev-fd657b0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 67.85% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x