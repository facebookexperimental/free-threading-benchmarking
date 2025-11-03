# Results vs. 3.13.0rc2

- fork: python
- ref: e66f87ca73516efb4aec
- machine: darwin-arm64
- commit hash: e66f87c
- commit date: 2025-11-02
- overall geometric mean: 1.034x faster
- HPT reliability: 97.18%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 229 ms: 2.30x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 229 ms: 2.27x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 232 ms: 1.67x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 43.0 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.2 ms: 2.88x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.18x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.1 ms: 1.08x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 48.0 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.94 ms: 1.08x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.6 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 888 ms: 1.13x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 100 us: 1.01x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (2): xml_etree_process, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.19 ms: 1.04x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.89 ms: 1.01x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 22.1 ms: 1.04x slower                                                    |
| mako            | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 229 ms: 2.30x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 229 ms: 2.27x faster                                                     |
| mdp                              | 1.06 sec                                                       | 536 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 232 ms: 1.67x faster                                                     |
| k_core                           | 1.46 sec                                                       | 901 ms: 1.62x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.2 us: 1.35x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.32x faster                                                     |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.0 ms: 1.31x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                     |
| go                               | 72.6 ms                                                        | 56.2 ms: 1.29x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                    |
| pyflate                          | 222 ms                                                         | 189 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 888 ms: 1.13x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 898 us: 1.11x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| float                            | 31.4 ms                                                        | 29.1 ms: 1.08x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.94 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.88 ms: 1.06x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.7 ms: 1.04x faster                                                    |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.2 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                                     |
| sphinx                           | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 43.0 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.01x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.76 ms: 1.01x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.02 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.45 ms: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.89 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 207 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 43.0 ms: 1.00x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 24.8 ms: 1.00x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 100 us: 1.01x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 325 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.6 ms: 1.01x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 660 ms: 1.02x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 418 us: 1.02x slower                                                     |
| pycparser                        | 470 ms                                                         | 479 ms: 1.02x slower                                                     |
| sqlite_synth                     | 948 ns                                                         | 967 ns: 1.02x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.03x slower                                                    |
| thrift                           | 309 us                                                         | 317 us: 1.03x slower                                                     |
| fannkuch                         | 179 ms                                                         | 183 ms: 1.03x slower                                                     |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 66.5 us: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.4 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.1 ms: 1.04x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.4 ms: 1.04x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.32 us: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.19 ms: 1.04x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.55 us: 1.04x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.5 ns: 1.05x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.6 ms: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                     |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.07x slower                                                    |
| raytrace                         | 109 ms                                                         | 117 ms: 1.08x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.3 ms: 1.08x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 40.7 ms: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.51 us: 1.10x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.3 ms: 1.11x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.8 ms: 1.12x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.7 ms: 1.13x slower                                                    |
| nbody                            | 42.5 ms                                                        | 48.0 ms: 1.13x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.16x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| many_optionals                   | 200 us                                                         | 367 us: 1.83x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.2 ms: 2.88x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.2 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (4): richards, xml_etree_process, hexiom, xml_etree_generate
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251102-3.15.0a1+-e66f87c/bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.034x faster

# HPT report

- Reliability score: 97.18% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.16x