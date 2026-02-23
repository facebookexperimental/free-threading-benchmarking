# Results vs. 3.12.6

- fork: python
- ref: fd01372d4e509b2cbec7
- machine: darwin-arm64
- commit hash: fd01372
- commit date: 2026-02-22
- overall geometric mean: 1.160x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 21.6 ms: 1.06x faster                                                    |
| sphinx         | 434 ms                                                   | 398 ms: 1.09x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 231 ms: 2.08x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 229 ms: 2.01x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 97.7 ms: 1.76x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.62x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| async_generators                 | 206 ms                                                   | 176 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.7 ms: 2.48x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.33x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.1 ms: 1.40x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.6 ms: 1.22x faster                                                    |
| pidigits       | 161 ms                                                   | 167 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                    | 1.18x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.4 ms: 1.18x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.0 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.69 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.1 ms: 1.32x faster                                                    |
| tomli_loads          | 957 ms                                                   | 840 ms: 1.14x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 99.9 us: 1.03x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (2): json_loads, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.99 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.49 ms: 1.14x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.13x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.55 ms: 1.10x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| mako            | 4.77 ms                                                  | 4.75 ms: 1.00x faster                                                    |
| django_template | 13.6 ms                                                  | 14.8 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.01 ms: 5.17x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 231 ms: 2.08x faster                                                     |
| mdp                              | 1.09 sec                                                 | 536 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 229 ms: 2.01x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 97.7 ms: 1.76x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                     |
| deepcopy                         | 161 us                                                   | 98.6 us: 1.64x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.62x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.8 us: 1.55x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.04 us: 1.40x faster                                                    |
| float                            | 37.9 ms                                                  | 27.1 ms: 1.40x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.08 us: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| go                               | 70.0 ms                                                  | 52.6 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.1 ms: 1.32x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 41.8 ms: 1.30x faster                                                    |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                     |
| k_core                           | 1.12 sec                                                 | 903 ms: 1.24x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 41.3 ns: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.8 ms: 1.22x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.6 ms: 1.22x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 119 ms: 1.19x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.18 us: 1.18x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.18x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.4 ms: 1.18x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.6 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.18x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.41 us: 1.16x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.8 ms: 1.16x faster                                                    |
| pyflate                          | 216 ms                                                   | 188 ms: 1.15x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 44.6 ms: 1.15x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.9 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.82 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 840 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.1 us: 1.12x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.3 ms: 1.11x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.0 ms: 1.10x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.76 ms: 1.10x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.55 ms: 1.10x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 398 ms: 1.09x faster                                                     |
| pycparser                        | 497 ms                                                   | 467 ms: 1.06x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.6 ms: 1.06x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.57 ms: 1.06x faster                                                    |
| thrift                           | 322 us                                                   | 307 us: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| fannkuch                         | 176 ms                                                   | 168 ms: 1.05x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 636 ms: 1.05x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 315 ms: 1.04x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 96.0 ms: 1.04x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 99.9 us: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.3 ms: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 946 ns: 1.02x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 38.1 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.75 ms: 1.00x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.69 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                     |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                     |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                     |
| pidigits                         | 161 ms                                                   | 167 ms: 1.03x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.09 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 50.2 ms: 1.05x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.80 ms: 1.07x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.8 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.99 ms: 1.12x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 933 us: 1.12x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.49 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.7 ms: 1.15x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.9 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 252 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.7 ms: 2.48x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |

Benchmark hidden because not significant (2): json_loads, pickle_pure_python
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260222-3.15.0a6+-fd01372/bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.160x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.23x