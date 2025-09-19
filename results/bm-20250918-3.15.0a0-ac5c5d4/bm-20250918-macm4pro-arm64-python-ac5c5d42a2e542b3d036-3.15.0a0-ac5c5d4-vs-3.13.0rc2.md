# Results vs. 3.13.0rc2

- fork: python
- ref: ac5c5d42a2e542b3d036
- machine: darwin-arm64
- commit hash: ac5c5d4
- commit date: 2025-09-18
- overall geometric mean: 1.016x faster
- HPT reliability: 87.12%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| html5lib       | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.83 ms: 1.09x faster                                                   |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.3 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.9 ms: 3.04x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.9 ms: 1.02x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 48.6 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.52 ms: 1.06x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.05x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 98.1 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 913 ms: 1.10x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.8 ms: 1.03x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 100 us: 1.01x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.6 ms: 1.01x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.01x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.21 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 22.2 ms: 1.04x slower                                                   |
| mako            | 4.41 ms                                                        | 5.02 ms: 1.14x slower                                                   |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| mdp                              | 1.06 sec                                                       | 538 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                    |
| k_core                           | 1.46 sec                                                       | 948 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.8 ms: 1.28x faster                                                   |
| go                               | 72.6 ms                                                        | 57.7 ms: 1.26x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                   |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 913 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.83 ms: 1.09x faster                                                   |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 925 us: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| telco                            | 3.07 ms                                                        | 2.87 ms: 1.07x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.52 ms: 1.06x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.05x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.8 ms: 1.03x faster                                                   |
| connected_components             | 208 ms                                                         | 203 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.3 ms: 1.02x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.6 ms: 1.02x faster                                                   |
| float                            | 31.4 ms                                                        | 30.9 ms: 1.02x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.3 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.45 ms: 1.01x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 64.1 us: 1.01x faster                                                   |
| json                             | 1.94 ms                                                        | 1.93 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.7 ms: 1.01x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 100 us: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.6 ms: 1.01x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 44.3 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.01x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 961 ns: 1.01x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.2 ns: 1.01x slower                                                   |
| thrift                           | 309 us                                                         | 314 us: 1.01x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.5 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 98.1 ms: 1.04x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.54 us: 1.04x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.32 us: 1.04x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 22.2 ms: 1.04x slower                                                   |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 677 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.21 ms: 1.04x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 336 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.05x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.54 ms: 1.06x slower                                                   |
| pycparser                        | 470 ms                                                         | 500 ms: 1.06x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.2 ms: 1.07x slower                                                   |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 51.2 ms: 1.07x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.90 ms: 1.07x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.0 ms: 1.07x slower                                                   |
| raytrace                         | 109 ms                                                         | 120 ms: 1.10x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.9 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.3 ms: 1.11x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.58 us: 1.11x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 42.5 ms: 1.12x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.13x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.02 ms: 1.14x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.7 ms: 1.14x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.6 ms: 1.14x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| many_optionals                   | 200 us                                                         | 329 us: 1.64x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.3 ms: 2.92x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.9 ms: 3.04x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (5): sphinx, docutils, hexiom, fannkuch, xml_etree_generate
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250918-3.15.0a0-ac5c5d4/bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.016x faster

# HPT report

- Reliability score: 87.12% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x