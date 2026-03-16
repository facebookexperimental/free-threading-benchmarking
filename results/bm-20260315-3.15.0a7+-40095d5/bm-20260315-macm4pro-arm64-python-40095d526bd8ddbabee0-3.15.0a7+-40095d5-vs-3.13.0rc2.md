# Results vs. 3.13.0rc2

- fork: python
- ref: 40095d526bd8ddbabee0
- machine: darwin-arm64
- commit hash: 40095d5
- commit date: 2026-03-15
- overall geometric mean: 1.079x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.3 ms: 1.09x faster                                                    |
| sphinx         | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 216 ms: 2.41x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 221 ms: 2.37x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 220 ms: 1.84x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 229 ms: 1.69x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.0 ms: 1.44x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 97.6 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.8 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.0 ms: 2.80x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.0 ms: 1.16x faster                                                    |
| nbody          | 42.5 ms                                                        | 44.8 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.63 ms: 1.11x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.3 ms: 1.03x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.79 ms: 1.23x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 825 ms: 1.21x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.9 ms: 1.18x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.02x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 99.8 us: 1.00x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 142 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.83 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.34 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.66 ms: 1.03x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.75 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 216 ms: 2.41x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 221 ms: 2.37x faster                                                     |
| mdp                              | 1.06 sec                                                       | 534 ms: 1.98x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 220 ms: 1.84x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 229 ms: 1.69x faster                                                     |
| k_core                           | 1.46 sec                                                       | 897 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.99 ms: 1.57x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.0 us: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.0 ms: 1.44x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.42x faster                                                    |
| go                               | 72.6 ms                                                        | 52.3 ms: 1.39x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 97.6 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.36x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.7 ms: 1.29x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.79 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 825 ms: 1.21x faster                                                     |
| pyflate                          | 222 ms                                                         | 184 ms: 1.21x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.9 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| float                            | 31.4 ms                                                        | 27.0 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.63 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.3 ms: 1.09x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 916 us: 1.08x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.8 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.84 ms: 1.08x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.4 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.7 ms: 1.08x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.2 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.04x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 119 ms: 1.04x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 42.1 ms: 1.04x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.3 ms: 1.03x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 36.0 ms: 1.03x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.66 ms: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.18 us: 1.03x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.40 us: 1.02x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.02x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 640 ms: 1.02x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 63.7 us: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 205 ms: 1.01x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 318 ms: 1.01x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.55 ms: 1.00x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 99.8 us: 1.00x slower                                                    |
| thrift                           | 309 us                                                         | 311 us: 1.01x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.80 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.7 ms: 1.02x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.83 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.04 us: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 426 us: 1.04x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 49.9 ms: 1.04x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.5 ms: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| nbody                            | 42.5 ms                                                        | 44.8 ms: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.34 ms: 1.07x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.2 ms: 1.07x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 46.0 ms: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.75 ms: 1.08x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 173 ms: 1.09x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 142 us: 1.09x slower                                                     |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.15x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 39.0 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.5 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.1 ms: 1.19x slower                                                    |
| many_optionals                   | 200 us                                                         | 251 us: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.0 ms: 2.80x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (4): sqlite_synth, pidigits, pycparser, logging_silent
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260315-3.15.0a7+-40095d5/bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.079x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.19x