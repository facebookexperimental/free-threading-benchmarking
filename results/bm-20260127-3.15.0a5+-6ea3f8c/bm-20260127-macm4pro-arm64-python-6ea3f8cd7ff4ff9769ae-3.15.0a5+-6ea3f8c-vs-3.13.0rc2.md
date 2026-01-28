# Results vs. 3.13.0rc2

- fork: python
- ref: 6ea3f8cd7ff4ff9769ae
- machine: darwin-arm64
- commit hash: 6ea3f8c
- commit date: 2026-01-27
- overall geometric mean: 1.100x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.01x faster                                                     |
| docutils       | 1.05 sec                                                       | 984 ms: 1.06x faster                                                     |
| html5lib       | 23.1 ms                                                        | 20.9 ms: 1.11x faster                                                    |
| sphinx         | 409 ms                                                         | 379 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 217 ms: 2.40x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 221 ms: 2.38x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 221 ms: 1.83x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 229 ms: 1.69x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.39x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 97.2 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 248 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| async_generators                 | 193 ms                                                         | 172 ms: 1.13x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.7 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.95 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 236 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.0 ms: 2.70x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.22x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.7 ms: 1.13x faster                                                    |
| pidigits       | 166 ms                                                         | 156 ms: 1.06x faster                                                     |
| nbody          | 42.5 ms                                                        | 43.6 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.47 ms: 1.13x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 44.7 ms: 1.07x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 92.8 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.73 ms: 1.25x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 825 ms: 1.21x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 33.8 ms: 1.06x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.0 ms: 1.06x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 95.6 us: 1.04x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 137 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.09x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.53 ms: 1.05x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.6 ms: 1.04x faster                                                    |
| mako            | 4.41 ms                                                        | 4.58 ms: 1.04x slower                                                    |
| django_template | 12.5 ms                                                        | 14.3 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 217 ms: 2.40x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 221 ms: 2.38x faster                                                     |
| mdp                              | 1.06 sec                                                       | 531 ms: 1.99x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 221 ms: 1.83x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 229 ms: 1.69x faster                                                     |
| k_core                           | 1.46 sec                                                       | 895 ms: 1.64x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.95 ms: 1.59x faster                                                    |
| deepcopy                         | 145 us                                                         | 96.3 us: 1.51x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.1 us: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| go                               | 72.6 ms                                                        | 51.6 ms: 1.41x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.39x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 97.2 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.34x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.1 ms: 1.30x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.73 ms: 1.25x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.05 us: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 248 ms: 1.21x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 825 ms: 1.21x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                     |
| pyflate                          | 222 ms                                                         | 186 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| richards                         | 22.1 ms                                                        | 19.4 ms: 1.14x faster                                                    |
| float                            | 31.4 ms                                                        | 27.7 ms: 1.13x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.47 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 172 ms: 1.13x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 21.9 ms: 1.13x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 892 us: 1.11x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 20.9 ms: 1.11x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 39.7 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.5 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.95 ms: 1.08x faster                                                    |
| sphinx                           | 409 ms                                                         | 379 ms: 1.08x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.86 ms: 1.07x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 44.7 ms: 1.07x faster                                                    |
| fannkuch                         | 179 ms                                                         | 167 ms: 1.07x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 301 ms: 1.07x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 610 ms: 1.07x faster                                                     |
| docutils                         | 1.05 sec                                                       | 984 ms: 1.06x faster                                                     |
| pidigits                         | 166 ms                                                         | 156 ms: 1.06x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 33.8 ms: 1.06x faster                                                    |
| json                             | 1.94 ms                                                        | 1.84 ms: 1.06x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.0 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.71 ms: 1.05x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 61.6 us: 1.05x faster                                                    |
| pycparser                        | 470 ms                                                         | 449 ms: 1.05x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.53 ms: 1.05x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.14 us: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 95.6 us: 1.04x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 20.6 ms: 1.04x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.25 ms: 1.04x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.36 us: 1.03x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                                     |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 1.99 ms: 1.03x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.41 ms: 1.03x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 92.8 ms: 1.02x faster                                                    |
| connected_components             | 208 ms                                                         | 205 ms: 1.01x faster                                                     |
| 2to3                             | 112 ms                                                         | 110 ms: 1.01x faster                                                     |
| logging_silent                   | 40.6 ns                                                        | 40.2 ns: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 941 ns: 1.01x faster                                                     |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| coverage                         | 31.2 ms                                                        | 31.5 ms: 1.01x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.2 ms: 1.01x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.91 us: 1.02x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 53.4 ms: 1.02x slower                                                    |
| nbody                            | 42.5 ms                                                        | 43.6 ms: 1.03x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.1 ms: 1.03x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 165 ms: 1.04x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.58 ms: 1.04x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.2 ms: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.04x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 137 us: 1.05x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 432 us: 1.05x slower                                                     |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 45.4 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.90 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 36.6 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 236 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.3 ms: 1.15x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 43.6 ms: 1.15x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.2 ms: 1.16x slower                                                    |
| many_optionals                   | 200 us                                                         | 245 us: 1.22x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.0 ms: 2.70x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                             |

Benchmark hidden because not significant (3): meteor_contest, nqueens, python_startup
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260127-3.15.0a5+-6ea3f8c/bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.18x