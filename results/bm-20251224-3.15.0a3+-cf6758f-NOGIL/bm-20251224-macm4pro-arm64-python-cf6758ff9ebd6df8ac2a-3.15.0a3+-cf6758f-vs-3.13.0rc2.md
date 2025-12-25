# Results vs. 3.13.0rc2

- fork: python
- ref: cf6758ff9ebd6df8ac2a
- machine: darwin-arm64
- commit hash: cf6758f
- commit date: 2025-12-24
- overall geometric mean: 1.015x faster
- HPT reliability: 53.13%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.07x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| sphinx         | 409 ms                                                         | 426 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 245 ms: 2.12x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 237 ms: 1.71x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 249 ms: 1.55x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.5 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.8 ms: 3.21x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.4 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.73 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.9 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.93 ms: 1.18x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 58.4 ms: 1.07x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 975 ms: 1.02x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 107 us: 1.07x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.81 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.12 ms: 1.20x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.2 ms: 1.08x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                    |
| mako            | 4.41 ms                                                        | 5.49 ms: 1.24x slower                                                    |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.18x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 802 us: 2.55x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 245 ms: 2.12x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 504 us: 1.97x faster                                                     |
| mdp                              | 1.06 sec                                                       | 606 ms: 1.74x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 237 ms: 1.71x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 249 ms: 1.55x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.05 ms: 1.55x faster                                                    |
| k_core                           | 1.46 sec                                                       | 994 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 108 us: 1.35x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.31x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| go                               | 72.6 ms                                                        | 59.3 ms: 1.22x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 53.6 ms: 1.19x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.93 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 821 ns: 1.15x faster                                                     |
| pyflate                          | 222 ms                                                         | 193 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.73 ms: 1.10x faster                                                    |
| float                            | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 58.4 ms: 1.07x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 975 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| pycparser                        | 470 ms                                                         | 466 ms: 1.01x faster                                                     |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.03x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 674 ms: 1.04x slower                                                     |
| richards                         | 22.1 ms                                                        | 22.9 ms: 1.04x slower                                                    |
| sphinx                           | 409 ms                                                         | 426 ms: 1.04x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.0 ms: 1.06x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.9 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 107 us: 1.07x slower                                                     |
| 2to3                             | 112 ms                                                         | 120 ms: 1.07x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.5 ms: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.9 ns: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.14 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.2 ms: 1.08x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.6 ms: 1.09x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 70.7 us: 1.09x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.45 us: 1.09x slower                                                    |
| thrift                           | 309 us                                                         | 339 us: 1.10x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.71 us: 1.11x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 252 ms: 1.12x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.13x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                    |
| pylint                           | 106 ms                                                         | 120 ms: 1.13x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.81 ms: 1.14x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.8 ms: 1.15x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.3 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.7 ms: 1.16x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.4 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.0 ms: 1.17x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.08 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.17x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.18x slower                                                     |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.12 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.5 ms: 1.20x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.24 us: 1.21x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.5 ms: 1.23x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.49 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 42.0 ms: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.25x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.7 ms: 1.32x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.4 ms: 1.33x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 547 us: 1.33x slower                                                     |
| many_optionals                   | 200 us                                                         | 268 us: 1.34x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 60.8 ms: 1.42x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.8 ms: 3.21x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (3): coroutines, html5lib, regex_dna
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251224-3.15.0a3+-cf6758f-NOGIL/bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.015x faster

# HPT report

- Reliability score: 53.13% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.30x