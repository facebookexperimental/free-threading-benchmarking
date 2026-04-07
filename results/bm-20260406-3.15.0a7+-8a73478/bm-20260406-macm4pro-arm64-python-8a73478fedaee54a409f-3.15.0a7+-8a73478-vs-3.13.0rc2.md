# Results vs. 3.13.0rc2

- fork: python
- ref: 8a73478fedaee54a409f
- machine: darwin-arm64
- commit hash: 8a73478
- commit date: 2026-04-06
- overall geometric mean: 1.089x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 993 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 21.0 ms: 1.10x faster                                                    |
| sphinx         | 409 ms                                                         | 390 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 218 ms: 2.39x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 221 ms: 2.37x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 224 ms: 1.81x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 230 ms: 1.68x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.37x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.35x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.2 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.8 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.98 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.5 ms: 2.78x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.5 ms: 1.19x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 43.3 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.57 ms: 1.12x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.7 ms: 1.05x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 94.0 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 802 ms: 1.25x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.7 ms: 1.19x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.2 ms: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 98.4 us: 1.01x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 137 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.48 ms: 1.05x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.7 ms: 1.03x faster                                                    |
| mako            | 4.41 ms                                                        | 4.72 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 218 ms: 2.39x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 221 ms: 2.37x faster                                                     |
| mdp                              | 1.06 sec                                                       | 526 ms: 2.01x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 224 ms: 1.81x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 230 ms: 1.68x faster                                                     |
| k_core                           | 1.46 sec                                                       | 896 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.98 ms: 1.57x faster                                                    |
| deepcopy                         | 145 us                                                         | 97.0 us: 1.50x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                    |
| go                               | 72.6 ms                                                        | 51.7 ms: 1.40x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.37x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.35x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.2 ms: 1.34x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.3 ms: 1.30x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 802 ms: 1.25x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.05 us: 1.23x faster                                                    |
| pyflate                          | 222 ms                                                         | 181 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.7 ms: 1.19x faster                                                    |
| float                            | 31.4 ms                                                        | 26.5 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.57 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.11x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.1 ms: 1.10x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.0 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| richards                         | 22.1 ms                                                        | 20.3 ms: 1.09x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.8 ms: 1.09x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.83 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 115 ms: 1.08x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.98 ms: 1.08x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.9 ms: 1.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 931 us: 1.07x faster                                                     |
| fannkuch                         | 179 ms                                                         | 168 ms: 1.06x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 41.5 ms: 1.05x faster                                                    |
| docutils                         | 1.05 sec                                                       | 993 ms: 1.05x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.48 ms: 1.05x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 45.7 ms: 1.05x faster                                                    |
| sphinx                           | 409 ms                                                         | 390 ms: 1.05x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.72 ms: 1.05x faster                                                    |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| json                             | 1.94 ms                                                        | 1.86 ms: 1.04x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.35 us: 1.04x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 60.2 ms: 1.04x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 630 ms: 1.03x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 20.7 ms: 1.03x faster                                                    |
| pycparser                        | 470 ms                                                         | 457 ms: 1.03x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 313 ms: 1.03x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.35 ms: 1.02x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.3 us: 1.02x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 36.8 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.4 us: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 94.0 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| deltablue                        | 1.45 ms                                                        | 1.45 ms: 1.00x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                    |
| thrift                           | 309 us                                                         | 311 us: 1.01x slower                                                     |
| chaos                            | 24.3 ms                                                        | 24.4 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                    |
| nbody                            | 42.5 ms                                                        | 43.3 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.81 ms: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.5 ns: 1.02x slower                                                    |
| raytrace                         | 109 ms                                                         | 112 ms: 1.02x slower                                                     |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 425 us: 1.03x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.2 ms: 1.03x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.4 ms: 1.04x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.08 us: 1.04x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 54.6 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.7 ms: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 137 us: 1.05x slower                                                     |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.72 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.0 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.3 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.7 ms: 1.18x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.42 ms: 1.19x slower                                                    |
| many_optionals                   | 200 us                                                         | 248 us: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.5 ms: 2.78x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.09x faster                                                             |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260406-3.15.0a7+-8a73478/bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.089x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.19x