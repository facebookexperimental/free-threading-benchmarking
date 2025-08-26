# Results vs. 3.13.0rc2

- fork: python
- ref: 95d6e0b2830c8e6bfd86
- machine: darwin-arm64
- commit hash: 95d6e0b
- commit date: 2025-08-25
- overall geometric mean: 1.006x faster
- HPT reliability: 71.87%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| docutils       | 1.05 sec                                                       | 994 ms: 1.05x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.8 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.8 ms: 1.13x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.8 ms: 2.69x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.6 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.4 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.0 ms: 1.01x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.2 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 36.9 ms: 1.25x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 3.93 ms: 1.18x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.2 ms: 1.09x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.13x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.50 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.91 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.3 ms: 1.14x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.8 ms: 1.18x slower                                                   |
| django_template | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| mako            | 4.41 ms                                                        | 5.88 ms: 1.33x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.24x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.66x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 778 us: 2.63x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 484 us: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| mdp                              | 1.06 sec                                                       | 605 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.8 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 988 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.9 ms: 1.25x faster                                                   |
| deepcopy                         | 145 us                                                         | 119 us: 1.22x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.21x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.93 ms: 1.18x faster                                                   |
| go                               | 72.6 ms                                                        | 62.0 ms: 1.17x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 14.2 us: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 817 ns: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 56.1 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| pyflate                          | 222 ms                                                         | 201 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 57.2 ms: 1.09x faster                                                   |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                    |
| float                            | 31.4 ms                                                        | 29.6 ms: 1.06x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.02 sec: 1.06x faster                                                  |
| docutils                         | 1.05 sec                                                       | 994 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                   |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 473 ms: 1.01x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                   |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| dask                             | 525 ms                                                         | 532 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.0 ms: 1.01x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                   |
| fannkuch                         | 179 ms                                                         | 185 ms: 1.04x slower                                                    |
| shortest_path                    | 225 ms                                                         | 236 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.97 ms: 1.06x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.6 ms: 1.07x slower                                                   |
| thrift                           | 309 us                                                         | 333 us: 1.08x slower                                                    |
| connected_components             | 208 ms                                                         | 224 ms: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.9 ms: 1.09x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.50 ms: 1.10x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 355 ms: 1.10x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.14 ms: 1.10x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 45.0 ns: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.2 ms: 1.11x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 721 ms: 1.11x slower                                                    |
| 2to3                             | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.50 us: 1.12x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.75 us: 1.12x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.13x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.8 ms: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.5 us: 1.14x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.3 ms: 1.14x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.1 ms: 1.14x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 50.0 ms: 1.14x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.91 ms: 1.16x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.9 ms: 1.16x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.17x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.5 ms: 1.17x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.3 ms: 1.17x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 145 ms: 1.17x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.8 ms: 1.18x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.6 ms: 1.18x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                    |
| raytrace                         | 109 ms                                                         | 132 ms: 1.21x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.5 ms: 1.22x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.2 ms: 1.22x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.38 us: 1.23x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.2 ms: 1.29x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.1 ms: 1.29x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.30 ms: 1.29x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 56.6 ms: 1.32x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.4 ms: 1.33x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.88 ms: 1.33x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 591 us: 1.44x slower                                                    |
| many_optionals                   | 200 us                                                         | 334 us: 1.66x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.8 ms: 2.69x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.4 ms: 2.94x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (2): sphinx, tomli_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250825-3.15.0a0-95d6e0b-NOGIL/bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.006x faster

# HPT report

- Reliability score: 71.87% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x