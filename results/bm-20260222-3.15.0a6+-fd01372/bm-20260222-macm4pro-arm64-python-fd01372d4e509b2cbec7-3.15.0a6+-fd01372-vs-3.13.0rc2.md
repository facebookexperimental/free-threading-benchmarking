# Results vs. 3.13.0rc2

- fork: python
- ref: fd01372d4e509b2cbec7
- machine: darwin-arm64
- commit hash: fd01372
- commit date: 2026-02-22
- overall geometric mean: 1.076x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                    |
| sphinx         | 409 ms                                                         | 398 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 223 ms: 2.36x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 223 ms: 2.34x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 231 ms: 1.75x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 229 ms: 1.69x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.40x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 97.7 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.34x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.7 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                    |
| pidigits       | 166 ms                                                         | 167 ms: 1.00x slower                                                     |
| nbody          | 42.5 ms                                                        | 44.6 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.69 ms: 1.10x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.4 ms: 1.03x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.0 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.77 ms: 1.23x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 840 ms: 1.19x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.1 ms: 1.18x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.5 ms: 1.04x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.7 ms: 1.03x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 99.9 us: 1.00x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.99 ms: 1.04x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.49 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.55 ms: 1.04x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| mako            | 4.41 ms                                                        | 4.75 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 14.8 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 223 ms: 2.36x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 223 ms: 2.34x faster                                                     |
| mdp                              | 1.06 sec                                                       | 536 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 231 ms: 1.75x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 229 ms: 1.69x faster                                                     |
| k_core                           | 1.46 sec                                                       | 903 ms: 1.62x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.01 ms: 1.56x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.6 us: 1.47x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.40x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.39x faster                                                    |
| go                               | 72.6 ms                                                        | 52.6 ms: 1.38x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 97.7 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.34x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.8 ms: 1.28x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.77 ms: 1.23x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.19x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 840 ms: 1.19x faster                                                     |
| pyflate                          | 222 ms                                                         | 188 ms: 1.18x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.1 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| float                            | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.69 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.80 ms: 1.10x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.3 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.8 ms: 1.08x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.0 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                    |
| fannkuch                         | 179 ms                                                         | 168 ms: 1.07x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 933 us: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.06x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 41.8 ms: 1.05x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.55 ms: 1.04x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 119 ms: 1.04x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.5 ms: 1.04x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.4 ms: 1.03x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.76 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 60.7 ms: 1.03x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.18 us: 1.03x faster                                                    |
| sphinx                           | 409 ms                                                         | 398 ms: 1.03x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 63.1 us: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 315 ms: 1.02x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 636 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.41 us: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| thrift                           | 309 us                                                         | 307 us: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| connected_components             | 208 ms                                                         | 207 ms: 1.00x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 99.9 us: 1.00x slower                                                    |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.00x slower                                                     |
| pidigits                         | 166 ms                                                         | 167 ms: 1.00x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.57 ms: 1.01x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.6 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.0 ms: 1.01x slower                                                    |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 41.3 ns: 1.02x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.9 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.09 ms: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.9 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.82 ms: 1.02x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.04 us: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                     |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 44.6 ms: 1.04x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.99 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.2 ms: 1.05x slower                                                    |
| nbody                            | 42.5 ms                                                        | 44.6 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.07x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.3 ms: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.75 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.49 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 38.1 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.8 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.7 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 252 us: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.7 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (3): pycparser, sqlite_synth, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260222-3.15.0a6+-fd01372/bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.076x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.19x