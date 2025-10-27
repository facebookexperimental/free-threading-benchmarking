# Results vs. 3.13.0rc2

- fork: python
- ref: 3dab11f888fda34c0273
- machine: darwin-arm64
- commit hash: 3dab11f
- commit date: 2025-10-26
- overall geometric mean: 1.025x faster
- HPT reliability: 88.83%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                   |
| sphinx         | 409 ms                                                         | 405 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 229 ms: 2.29x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 231 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 232 ms: 1.67x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 141 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 142 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 42.8 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.2 ms: 2.87x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.17x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 50.0 ms: 1.18x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.12x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.86 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.0 ms: 1.18x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.99 ms: 1.17x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 900 ms: 1.11x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 60.3 ms: 1.03x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.01x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.81 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.9 ms: 1.02x slower                                                    |
| mako            | 4.41 ms                                                        | 4.88 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 229 ms: 2.29x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 231 ms: 2.26x faster                                                     |
| mdp                              | 1.06 sec                                                       | 541 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 232 ms: 1.67x faster                                                     |
| k_core                           | 1.46 sec                                                       | 902 ms: 1.62x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.2 us: 1.35x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 141 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                     |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 142 ms: 1.29x faster                                                     |
| go                               | 72.6 ms                                                        | 56.1 ms: 1.29x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.0 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.99 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                     |
| pyflate                          | 222 ms                                                         | 194 ms: 1.15x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.12x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.11x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 900 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| float                            | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.86 ms: 1.09x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.91 ms: 1.05x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.02 sec: 1.05x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 945 us: 1.05x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.3 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| richards                         | 22.1 ms                                                        | 21.5 ms: 1.03x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.2 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 24.2 ms: 1.02x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                    |
| connected_components             | 208 ms                                                         | 205 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 164 ms: 1.02x faster                                                     |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.01x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.5 ms: 1.01x faster                                                    |
| sphinx                           | 409 ms                                                         | 405 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 42.8 ms: 1.01x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.84 ms: 1.00x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                     |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 417 us: 1.01x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.81 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 66.1 us: 1.02x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.9 ms: 1.02x slower                                                    |
| thrift                           | 309 us                                                         | 317 us: 1.02x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 667 ms: 1.03x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.03x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 977 ns: 1.03x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 332 ms: 1.03x slower                                                     |
| fannkuch                         | 179 ms                                                         | 185 ms: 1.04x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 42.0 ns: 1.04x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.3 ms: 1.04x slower                                                    |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.2 ms: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.87 ms: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.58 us: 1.06x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.7 ms: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                     |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                     |
| pycparser                        | 470 ms                                                         | 509 ms: 1.08x slower                                                     |
| chaos                            | 24.3 ms                                                        | 26.3 ms: 1.08x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 41.2 ms: 1.09x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 57.4 ms: 1.10x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.88 ms: 1.11x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.55 us: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 48.2 ms: 1.13x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.0 ms: 1.13x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.2 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| nbody                            | 42.5 ms                                                        | 50.0 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 376 us: 1.88x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.2 ms: 2.87x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.2 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (8): xml_etree_generate, dask, json, async_tree_eager_cpu_io_mixed, spectral_norm, sympy_integrate, html5lib, genshi_text
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251026-3.15.0a1+-3dab11f/bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.025x faster

# HPT report

- Reliability score: 88.83% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.15x