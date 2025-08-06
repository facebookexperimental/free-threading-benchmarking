# Results vs. 3.13.0rc2

- fork: python
- ref: c2428ca9ea0c4eac9c7f
- machine: darwin-arm64
- commit hash: c2428ca
- commit date: 2025-08-05
- overall geometric mean: 1.004x faster
- HPT reliability: 83.74%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 996 ms: 1.05x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| sphinx         | 409 ms                                                         | 417 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.6 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.8 ms: 1.43x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 225 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.4 ms: 1.10x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.1 ms: 2.66x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                   |
| nbody          | 42.5 ms                                                        | 61.2 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                          | 1.10x slower                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.0 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.1 ms: 1.18x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.3 ms: 1.03x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.57 ms: 1.02x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 1.01 sec: 1.01x slower                                                  |
| xml_etree_generate   | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.08x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.13x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.59 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.97 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.15x slower                                                   |
| mako            | 4.41 ms                                                        | 5.70 ms: 1.29x slower                                                   |
| django_template | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 768 us: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 480 us: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| mdp                              | 1.06 sec                                                       | 599 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.6 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 985 ms: 1.49x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.8 ms: 1.43x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                    |
| deepcopy                         | 145 us                                                         | 119 us: 1.22x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.9 us: 1.18x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.1 ms: 1.18x faster                                                   |
| go                               | 72.6 ms                                                        | 61.6 ms: 1.18x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 820 ns: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 56.1 ms: 1.14x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.12x faster                                                    |
| pyflate                          | 222 ms                                                         | 199 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| float                            | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                   |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                    |
| docutils                         | 1.05 sec                                                       | 996 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.3 ms: 1.03x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.57 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| tomli_loads                      | 1000 ms                                                        | 1.01 sec: 1.01x slower                                                  |
| sphinx                           | 409 ms                                                         | 417 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 232 ms: 1.03x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 221 ms: 1.06x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.25 ms: 1.06x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.03 ms: 1.07x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.08x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.8 ms: 1.08x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 225 ms: 1.08x slower                                                    |
| thrift                           | 309 us                                                         | 335 us: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.1 ns: 1.09x slower                                                   |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.4 ms: 1.10x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.13 ms: 1.10x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.0 ms: 1.11x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 356 ms: 1.11x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.59 ms: 1.11x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 726 ms: 1.12x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.6 ms: 1.12x slower                                                   |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.3 us: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.0 ms: 1.14x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.15x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 42.7 ms: 1.15x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.57 us: 1.15x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.84 us: 1.16x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 144 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.97 ms: 1.17x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.6 ms: 1.18x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.4 ms: 1.18x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.9 ms: 1.19x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.0 ms: 1.19x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.24 us: 1.21x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.5 ms: 1.21x slower                                                   |
| raytrace                         | 109 ms                                                         | 133 ms: 1.23x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.8 ms: 1.27x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.27 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.1 ms: 1.29x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.70 ms: 1.29x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 58.0 ms: 1.36x slower                                                   |
| nbody                            | 42.5 ms                                                        | 61.2 ms: 1.44x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 600 us: 1.46x slower                                                    |
| many_optionals                   | 200 us                                                         | 331 us: 1.65x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.1 ms: 2.66x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.3 ms: 2.92x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (3): fannkuch, pycparser, pidigits
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 83.74% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x