# Results vs. 3.13.0rc2

- fork: python
- ref: be9c7cb4b50f8007b610
- machine: darwin-arm64
- commit hash: be9c7cb
- commit date: 2026-05-01
- overall geometric mean: 1.046x faster
- HPT reliability: 99.92%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| docutils       | 1.05 sec                                                       | 969 ms: 1.08x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.2 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 309 ms: 1.70x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 335 ms: 1.55x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 309 ms: 1.25x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 328 ms: 1.23x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 120 ms: 1.19x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.89 ms: 1.09x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.2 ms: 1.07x faster                                                    |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 282 ms: 1.04x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 292 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 263 ms: 1.27x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 152 ms: 1.48x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 102 ms: 3.54x slower                                                     |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.4 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.73 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.7 ms: 1.05x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.1 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.74 ms: 1.24x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 820 ms: 1.22x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.0 ms: 1.07x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.2 ms: 1.00x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.9 ms: 1.00x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 100 us: 1.01x slower                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 66.6 ms: 1.07x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 5.93 ms: 1.00x faster                                                    |
| python_startup         | 8.63 ms                                                        | 8.77 ms: 1.02x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.89 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.20x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.15x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 540 ms: 1.96x faster                                                     |
| pylint                           | 106 ms                                                         | 57.0 ms: 1.85x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 309 ms: 1.70x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 335 ms: 1.55x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.05 ms: 1.55x faster                                                    |
| k_core                           | 1.46 sec                                                       | 979 ms: 1.50x faster                                                     |
| deepcopy                         | 145 us                                                         | 99.1 us: 1.46x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                    |
| go                               | 72.6 ms                                                        | 53.0 ms: 1.37x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.1 ms: 1.25x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 309 ms: 1.25x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.74 ms: 1.24x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 328 ms: 1.23x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 820 ms: 1.22x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                    |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 120 ms: 1.19x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 874 us: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.73 ms: 1.10x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.79 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.89 ms: 1.09x faster                                                    |
| fannkuch                         | 179 ms                                                         | 165 ms: 1.09x faster                                                     |
| docutils                         | 1.05 sec                                                       | 969 ms: 1.08x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.2 ms: 1.07x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.0 ms: 1.07x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.6 ms: 1.07x faster                                                    |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                     |
| nqueens                          | 37.2 ms                                                        | 35.0 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.3 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 305 ms: 1.06x faster                                                     |
| float                            | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.4 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 45.7 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 1.95 ms: 1.04x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 623 ms: 1.04x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.2 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 282 ms: 1.04x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 119 ms: 1.04x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 62.2 us: 1.04x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 292 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 39.7 ns: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 927 ns: 1.02x faster                                                     |
| connected_components             | 208 ms                                                         | 205 ms: 1.01x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.44 ms: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 43.4 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.00x faster                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 5.93 ms: 1.00x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.9 ms: 1.00x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.1 ms: 1.01x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.01x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 100 us: 1.01x slower                                                     |
| chaos                            | 24.3 ms                                                        | 24.6 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.77 ms: 1.02x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.97 us: 1.02x slower                                                    |
| pycparser                        | 470 ms                                                         | 484 ms: 1.03x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 98.5 ms: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 54.5 ms: 1.04x slower                                                    |
| nbody                            | 42.5 ms                                                        | 44.4 ms: 1.05x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.1 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                     |
| raytrace                         | 109 ms                                                         | 115 ms: 1.05x slower                                                     |
| 2to3                             | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 66.6 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.08x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.92 ms: 1.08x slower                                                    |
| coverage                         | 31.2 ms                                                        | 34.2 ms: 1.10x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.89 ms: 1.11x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.6 ms: 1.12x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 48.4 ms: 1.13x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 39.3 ms: 1.17x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.5 ms: 1.26x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 263 ms: 1.27x slower                                                     |
| many_optionals                   | 200 us                                                         | 256 us: 1.28x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 152 ms: 1.48x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 102 ms: 3.54x slower                                                     |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (6): sphinx, json_loads, logging_format, logging_simple, async_tree_eager_cpu_io_mixed, thrift
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260501-3.15.0a8+-be9c7cb/bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.046x faster

# HPT report

- Reliability score: 99.92% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x