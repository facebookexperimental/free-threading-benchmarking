# Results vs. 3.13.0rc2

- fork: python
- ref: 945bf8ce1bf7ee388175
- machine: darwin-arm64
- commit hash: 945bf8c
- commit date: 2026-02-12
- overall geometric mean: 1.080x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.3 ms: 1.08x faster                                                    |
| sphinx         | 409 ms                                                         | 391 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 221 ms: 2.38x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.34x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 225 ms: 1.72x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 96.7 ms: 1.37x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 257 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.5 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 236 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.5 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.4 ms: 1.15x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 45.7 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.61 ms: 1.11x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.0 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|---------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps          | 4.65 ms                                                        | 3.80 ms: 1.22x faster                                                    |
| tomli_loads         | 1000 ms                                                        | 834 ms: 1.20x faster                                                     |
| xml_etree_iterparse | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                    |
| xml_etree_parse     | 62.4 ms                                                        | 59.6 ms: 1.05x faster                                                    |
| xml_etree_process   | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| xml_etree_generate  | 35.8 ms                                                        | 34.6 ms: 1.04x faster                                                    |
| json_loads          | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| pickle_pure_python  | 130 us                                                         | 140 us: 1.07x slower                                                     |
| Geometric mean      | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.79 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.34 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.55 ms: 1.04x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.1 ms: 1.02x faster                                                    |
| mako            | 4.41 ms                                                        | 4.72 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 221 ms: 2.38x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.34x faster                                                     |
| mdp                              | 1.06 sec                                                       | 530 ms: 2.00x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 225 ms: 1.72x faster                                                     |
| k_core                           | 1.46 sec                                                       | 893 ms: 1.64x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.07 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.0 us: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 96.7 ms: 1.37x faster                                                    |
| go                               | 72.6 ms                                                        | 53.4 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.34x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.2 ms: 1.30x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.80 ms: 1.22x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 834 ms: 1.20x faster                                                     |
| pyflate                          | 222 ms                                                         | 187 ms: 1.19x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| float                            | 31.4 ms                                                        | 27.4 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 257 ms: 1.14x faster                                                     |
| richards                         | 22.1 ms                                                        | 19.8 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.61 ms: 1.11x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.4 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 912 us: 1.09x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 21.3 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.84 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.5 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 59.6 ms: 1.05x faster                                                    |
| sphinx                           | 409 ms                                                         | 391 ms: 1.05x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 118 ms: 1.04x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.55 ms: 1.04x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.0 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 310 ms: 1.04x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.6 ms: 1.04x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 628 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 63.1 us: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| pycparser                        | 470 ms                                                         | 460 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.1 ms: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.41 ms: 1.02x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 936 ns: 1.01x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.43 us: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                     |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.05 ms: 1.00x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.5 ms: 1.01x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.3 ns: 1.02x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.79 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.82 ms: 1.02x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.2 ms: 1.03x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.98 us: 1.03x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.3 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.6 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.05x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.1 ms: 1.05x slower                                                    |
| raytrace                         | 109 ms                                                         | 115 ms: 1.06x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.34 ms: 1.07x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.72 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.07x slower                                                     |
| nbody                            | 42.5 ms                                                        | 45.7 ms: 1.07x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 38.1 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 236 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.7 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.5 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 255 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.5 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (5): regex_dna, connected_components, thrift, unpickle_pure_python, spectral_norm
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260212-3.15.0a6+-945bf8c/bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.080x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.18x