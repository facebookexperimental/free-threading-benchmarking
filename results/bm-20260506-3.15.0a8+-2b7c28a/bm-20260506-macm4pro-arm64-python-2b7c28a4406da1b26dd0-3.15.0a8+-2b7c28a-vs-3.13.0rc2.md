# Results vs. 3.13.0rc2

- fork: python
- ref: 2b7c28a4406da1b26dd0
- machine: darwin-arm64
- commit hash: 2b7c28a
- commit date: 2026-05-06
- overall geometric mean: 1.068x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 950 ms: 1.10x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                    |
| sphinx         | 409 ms                                                         | 402 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 302 ms: 1.74x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 328 ms: 1.59x faster                                                     |
| async_generators                 | 193 ms                                                         | 143 ms: 1.35x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 302 ms: 1.28x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 321 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 169 ms: 1.10x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.4 ms: 1.10x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 122 ms: 1.08x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.97 ms: 1.08x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 274 ms: 1.07x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 173 ms: 1.07x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 284 ms: 1.06x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 256 ms: 1.23x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 149 ms: 1.45x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 99.7 ms: 3.45x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.4 ms: 1.07x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 43.7 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.58 ms: 1.12x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.3 ms: 1.06x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.5 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.67 ms: 1.27x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 823 ms: 1.22x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.7 ms: 1.13x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 97.0 us: 1.03x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 64.7 ms: 1.04x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 138 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 14.4 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 508 ms: 2.08x faster                                                     |
| pylint                           | 106 ms                                                         | 55.8 ms: 1.89x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 302 ms: 1.74x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 328 ms: 1.59x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.09 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.1 us: 1.48x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.45x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.40x faster                                                    |
| go                               | 72.6 ms                                                        | 51.9 ms: 1.40x faster                                                    |
| async_generators                 | 193 ms                                                         | 143 ms: 1.35x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 48.9 ms: 1.31x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 302 ms: 1.28x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.67 ms: 1.27x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 321 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 823 ms: 1.22x faster                                                     |
| pyflate                          | 222 ms                                                         | 183 ms: 1.21x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 856 us: 1.16x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.7 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.58 ms: 1.12x faster                                                    |
| docutils                         | 1.05 sec                                                       | 950 ms: 1.10x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 169 ms: 1.10x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.4 ms: 1.10x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 122 ms: 1.08x faster                                                     |
| richards                         | 22.1 ms                                                        | 20.4 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.84 ms: 1.08x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.97 ms: 1.08x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 274 ms: 1.07x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                    |
| float                            | 31.4 ms                                                        | 29.4 ms: 1.07x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 173 ms: 1.07x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 23.2 ms: 1.06x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 1.92 ms: 1.06x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 117 ms: 1.06x faster                                                     |
| nqueens                          | 37.2 ms                                                        | 35.1 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 284 ms: 1.06x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 45.3 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                     |
| fannkuch                         | 179 ms                                                         | 169 ms: 1.06x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 306 ms: 1.05x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                    |
| json                             | 1.94 ms                                                        | 1.85 ms: 1.05x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.72 ms: 1.05x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 622 ms: 1.04x faster                                                     |
| logging_silent                   | 40.6 ns                                                        | 38.9 ns: 1.04x faster                                                    |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.36 us: 1.04x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.17 us: 1.03x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.31 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 97.0 us: 1.03x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.4 us: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 402 ms: 1.02x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 43.1 ms: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 936 ns: 1.01x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 93.5 ms: 1.01x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                     |
| chaos                            | 24.3 ms                                                        | 24.2 ms: 1.00x faster                                                    |
| connected_components             | 208 ms                                                         | 207 ms: 1.00x faster                                                     |
| shortest_path                    | 225 ms                                                         | 225 ms: 1.00x slower                                                     |
| pycparser                        | 470 ms                                                         | 476 ms: 1.01x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 48.9 ms: 1.02x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.96 us: 1.02x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.0 ms: 1.03x slower                                                    |
| nbody                            | 42.5 ms                                                        | 43.7 ms: 1.03x slower                                                    |
| raytrace                         | 109 ms                                                         | 112 ms: 1.03x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 426 us: 1.03x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.3 ms: 1.04x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 54.2 ms: 1.04x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 64.7 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.85 ms: 1.04x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 138 us: 1.06x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 46.3 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.6 ms: 1.15x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.4 ms: 1.16x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.2 ms: 1.16x slower                                                    |
| many_optionals                   | 200 us                                                         | 236 us: 1.18x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 46.3 ms: 1.22x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 256 ms: 1.23x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 149 ms: 1.45x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 99.7 ms: 3.45x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (3): deltablue, thrift, xml_etree_generate
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260506-3.15.0a8+-2b7c28a/bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.068x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.17x