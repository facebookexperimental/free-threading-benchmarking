# Results vs. 3.13.0rc2

- fork: python
- ref: 5fe139cc39fb8110b3d6
- machine: darwin-arm64
- commit hash: 5fe139c
- commit date: 2026-02-15
- overall geometric mean: 1.076x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                    |
| sphinx         | 409 ms                                                         | 394 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.40x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.36x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 225 ms: 1.72x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.39x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 97.3 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.1 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 234 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.5 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 45.0 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.71 ms: 1.10x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.5 ms: 1.05x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.1 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 847 ms: 1.18x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.7 ms: 1.13x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.5 ms: 1.04x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 97.6 us: 1.02x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.91 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.43 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.64 ms: 1.03x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.40x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.36x faster                                                     |
| mdp                              | 1.06 sec                                                       | 537 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 225 ms: 1.72x faster                                                     |
| k_core                           | 1.46 sec                                                       | 900 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.96 ms: 1.58x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.2 us: 1.48x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.44x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.39x faster                                                     |
| go                               | 72.6 ms                                                        | 53.0 ms: 1.37x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 97.3 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.35x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.0 ms: 1.28x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 847 ms: 1.18x faster                                                     |
| pyflate                          | 222 ms                                                         | 192 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.7 ms: 1.13x faster                                                    |
| float                            | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.71 ms: 1.10x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.4 ms: 1.10x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.1 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 914 us: 1.09x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.83 ms: 1.08x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.1 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.1 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 168 ms: 1.06x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 45.5 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| sphinx                           | 409 ms                                                         | 394 ms: 1.04x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.75 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 311 ms: 1.04x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.5 ms: 1.04x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 628 ms: 1.04x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.64 ms: 1.03x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 97.6 us: 1.02x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 121 ms: 1.02x faster                                                     |
| connected_components             | 208 ms                                                         | 205 ms: 1.02x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 64.0 us: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.01x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                    |
| thrift                           | 309 us                                                         | 311 us: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 96.1 ms: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.3 ns: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.9 ms: 1.02x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.00 us: 1.03x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.91 ms: 1.03x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 45.2 ms: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 39.2 ms: 1.05x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.5 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                     |
| nbody                            | 42.5 ms                                                        | 45.0 ms: 1.06x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.7 ms: 1.07x slower                                                    |
| raytrace                         | 109 ms                                                         | 116 ms: 1.07x slower                                                     |
| chaos                            | 24.3 ms                                                        | 26.0 ms: 1.07x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 171 ms: 1.07x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.08x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 46.1 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.43 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.92 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 234 ms: 1.12x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.8 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.4 ms: 1.17x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.4 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 249 us: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.5 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (7): pycparser, logging_simple, logging_format, sqlite_synth, sympy_integrate, 2to3, xml_etree_parse
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260215-3.15.0a6+-5fe139c/bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.076x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.19x