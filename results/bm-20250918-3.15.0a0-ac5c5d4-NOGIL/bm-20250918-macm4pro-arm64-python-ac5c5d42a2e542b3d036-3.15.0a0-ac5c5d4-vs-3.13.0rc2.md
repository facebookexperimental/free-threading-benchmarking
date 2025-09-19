# Results vs. 3.13.0rc2

- fork: python
- ref: ac5c5d42a2e542b3d036
- machine: darwin-arm64
- commit hash: ac5c5d4
- commit date: 2025-09-18
- overall geometric mean: 1.012x faster
- HPT reliability: 62.24%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 979 ms: 1.07x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.06x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.0 ms: 1.54x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.0 ms: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 225 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.7 ms: 1.13x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.5 ms: 2.68x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| nbody          | 42.5 ms                                                        | 57.0 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.1 ms: 1.00x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.0 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.6 ms: 1.23x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 3.92 ms: 1.19x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 958 ms: 1.04x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.13x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.52 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.92 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.0 ms: 1.12x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.6 ms: 1.17x slower                                                   |
| django_template | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                   |
| mako            | 4.41 ms                                                        | 5.84 ms: 1.32x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.23x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 759 us: 2.69x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 472 us: 2.10x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.06x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.85x faster                                                    |
| mdp                              | 1.06 sec                                                       | 601 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.0 ms: 1.54x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.0 ms: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                    |
| deepcopy                         | 145 us                                                         | 115 us: 1.26x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.25x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.6 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.92 ms: 1.19x faster                                                   |
| go                               | 72.6 ms                                                        | 61.7 ms: 1.18x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.1 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 820 ns: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| pyflate                          | 222 ms                                                         | 199 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                  |
| docutils                         | 1.05 sec                                                       | 979 ms: 1.07x faster                                                    |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                   |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 958 ms: 1.04x faster                                                    |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.26 us: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.03 ms: 1.01x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 95.1 ms: 1.00x slower                                                   |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                                   |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                   |
| fannkuch                         | 179 ms                                                         | 186 ms: 1.04x slower                                                    |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.99 ms: 1.06x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.5 ms: 1.07x slower                                                   |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                    |
| connected_components             | 208 ms                                                         | 222 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 225 ms: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.8 ms: 1.08x slower                                                   |
| thrift                           | 309 us                                                         | 335 us: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.09x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 352 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 716 ms: 1.10x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.14 ms: 1.10x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.52 ms: 1.10x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.0 ms: 1.11x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 42.0 ms: 1.11x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 45.3 ns: 1.11x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.50 us: 1.12x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.0 ms: 1.12x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.13x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.7 ms: 1.13x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.79 us: 1.14x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.1 ms: 1.14x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 142 ms: 1.15x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 74.3 us: 1.15x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.92 ms: 1.16x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.6 ms: 1.17x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.1 ms: 1.17x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.1 ms: 1.17x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.4 ms: 1.17x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 43.8 ms: 1.17x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.3 ms: 1.21x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.21x slower                                                   |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.35 us: 1.23x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.0 ms: 1.28x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.28 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.1 ms: 1.28x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.84 ms: 1.32x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 57.0 ms: 1.33x slower                                                   |
| nbody                            | 42.5 ms                                                        | 57.0 ms: 1.34x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 589 us: 1.43x slower                                                    |
| many_optionals                   | 200 us                                                         | 331 us: 1.65x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.5 ms: 2.68x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.8 ms: 3.00x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (2): sphinx, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250918-3.15.0a0-ac5c5d4-NOGIL/bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 62.24% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x