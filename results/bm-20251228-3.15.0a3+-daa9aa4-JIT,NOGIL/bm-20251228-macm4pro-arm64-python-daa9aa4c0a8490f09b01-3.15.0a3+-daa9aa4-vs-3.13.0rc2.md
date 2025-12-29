# Results vs. 3.13.0rc2

- fork: python
- ref: daa9aa4c0a8490f09b01
- machine: darwin-arm64
- commit hash: daa9aa4
- commit date: 2025-12-28
- overall geometric mean: 1.006x slower
- HPT reliability: 86.74%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                    |
| sphinx         | 409 ms                                                         | 433 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 256 ms: 2.05x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 242 ms: 1.67x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.21x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| async_generators                 | 193 ms                                                         | 189 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.1 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 95.2 ms: 3.29x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.1 ms: 1.08x faster                                                    |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                     |
| nbody          | 42.5 ms                                                        | 58.2 ms: 1.37x slower                                                    |
| Geometric mean | (ref)                                                          | 1.09x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.35 ms: 1.14x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.9 ms: 1.02x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.7 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.9 ms: 1.19x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.07 ms: 1.14x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 1.02 sec: 1.02x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.7 ms: 1.05x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.6 ms: 1.09x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 149 us: 1.15x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.24 ms: 1.22x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.19x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.2 ms: 1.13x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.7 ms: 1.17x slower                                                    |
| mako            | 4.41 ms                                                        | 5.56 ms: 1.26x slower                                                    |
| django_template | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.22x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 819 us: 2.49x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 256 ms: 2.05x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 512 us: 1.94x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 242 ms: 1.67x faster                                                     |
| mdp                              | 1.06 sec                                                       | 635 ms: 1.67x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.22 ms: 1.48x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.45x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.30x faster                                                    |
| deepcopy                         | 145 us                                                         | 113 us: 1.28x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.21x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.20x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.9 ms: 1.19x faster                                                    |
| go                               | 72.6 ms                                                        | 61.2 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 825 ns: 1.15x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.8 ms: 1.15x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.35 ms: 1.14x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.07 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                    |
| float                            | 31.4 ms                                                        | 29.1 ms: 1.08x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.02 sec: 1.06x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.23 us: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.1 ms: 1.04x faster                                                    |
| async_generators                 | 193 ms                                                         | 189 ms: 1.02x faster                                                     |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 477 ms: 1.01x slower                                                     |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                     |
| tomli_loads                      | 1000 ms                                                        | 1.02 sec: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 96.9 ms: 1.02x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 127 ms: 1.02x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                    |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 338 ms: 1.05x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.7 ms: 1.05x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 688 ms: 1.06x slower                                                     |
| sphinx                           | 409 ms                                                         | 433 ms: 1.06x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.6 ms: 1.07x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.7 ms: 1.08x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.6 ms: 1.09x slower                                                    |
| thrift                           | 309 us                                                         | 339 us: 1.10x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 27.1 ms: 1.10x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.1 us: 1.10x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.9 ms: 1.10x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 45.0 ns: 1.11x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.35 ms: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.1 ms: 1.11x slower                                                    |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.52 us: 1.13x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 24.2 ms: 1.13x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.22 ms: 1.13x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.77 us: 1.13x slower                                                    |
| shortest_path                    | 225 ms                                                         | 257 ms: 1.15x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.15x slower                                                     |
| pylint                           | 106 ms                                                         | 122 ms: 1.16x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.68 ms: 1.16x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.7 ms: 1.17x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.5 ms: 1.17x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.4 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 129 ms: 1.19x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 113 ms: 1.19x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 57.1 ms: 1.19x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.19x slower                                                     |
| connected_components             | 208 ms                                                         | 249 ms: 1.20x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 192 ms: 1.20x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 63.2 ms: 1.21x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.16 ms: 1.21x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.24 ms: 1.22x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 45.9 ms: 1.23x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.7 ms: 1.24x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.56 ms: 1.26x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.60 us: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 43.0 ms: 1.28x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.0 ms: 1.28x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 551 us: 1.34x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 57.9 ms: 1.35x slower                                                    |
| generators                       | 15.7 ms                                                        | 21.3 ms: 1.35x slower                                                    |
| nbody                            | 42.5 ms                                                        | 58.2 ms: 1.37x slower                                                    |
| many_optionals                   | 200 us                                                         | 278 us: 1.39x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 95.2 ms: 3.29x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (2): async_tree_eager_cpu_io_mixed, telco
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251228-3.15.0a3+-daa9aa4-JIT,NOGIL/bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 86.74% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x