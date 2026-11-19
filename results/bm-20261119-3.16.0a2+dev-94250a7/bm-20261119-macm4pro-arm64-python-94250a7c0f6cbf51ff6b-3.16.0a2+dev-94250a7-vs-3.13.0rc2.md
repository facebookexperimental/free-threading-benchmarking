# Results vs. 3.13.0rc2

- fork: python
- ref: 94250a7c0f6cbf51ff6b
- machine: darwin-arm64
- commit hash: 94250a7
- commit date: 2026-11-19
- overall geometric mean: 1.103x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.02x slower                                                        |
| docutils       | 1.05 sec                                                       | 909 ms: 1.15x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.7 ms: 1.12x faster                                                       |
| sphinx         | 409 ms                                                         | 391 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 265 ms: 1.98x faster                                                        |
| async_generators                 | 193 ms                                                         | 97.7 ms: 1.98x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 277 ms: 1.88x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 278 ms: 1.46x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 271 ms: 1.42x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.19x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 158 ms: 1.18x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 162 ms: 1.14x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.64 ms: 1.12x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 271 ms: 1.11x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 142 ms: 1.38x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.8 ms: 3.24x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.0 ms: 1.16x faster                                                       |
| pidigits       | 166 ms                                                         | 149 ms: 1.11x faster                                                        |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.09 ms: 1.18x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 92.2 ms: 1.03x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 53.7 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.62 ms: 1.28x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 804 ms: 1.24x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.1 ms: 1.09x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 95.7 us: 1.04x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 66.8 ms: 1.07x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.07x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.31 ms: 1.04x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.47 ms: 1.09x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                                |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 501 ms: 2.11x faster                                                        |
| pylint                           | 106 ms                                                         | 52.0 ms: 2.03x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 265 ms: 1.98x faster                                                        |
| async_generators                 | 193 ms                                                         | 97.7 ms: 1.98x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 277 ms: 1.88x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.95 ms: 1.59x faster                                                       |
| create_gc_cycles                 | 993 us                                                         | 636 us: 1.56x faster                                                        |
| deepcopy                         | 145 us                                                         | 95.3 us: 1.52x faster                                                       |
| k_core                           | 1.46 sec                                                       | 981 ms: 1.49x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 278 ms: 1.46x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 45.3 us: 1.43x faster                                                       |
| async_tree_io                    | 386 ms                                                         | 271 ms: 1.42x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                       |
| go                               | 72.6 ms                                                        | 52.0 ms: 1.39x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 49.2 ms: 1.30x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.62 ms: 1.28x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 804 ms: 1.24x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.04 us: 1.24x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| pyflate                          | 222 ms                                                         | 184 ms: 1.21x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.19x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 158 ms: 1.18x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.09 ms: 1.18x faster                                                       |
| float                            | 31.4 ms                                                        | 27.0 ms: 1.16x faster                                                       |
| docutils                         | 1.05 sec                                                       | 909 ms: 1.15x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.0 ms: 1.15x faster                                                       |
| gc_traversal                     | 2.04 ms                                                        | 1.79 ms: 1.14x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.87 sec: 1.14x faster                                                      |
| async_tree_memoization           | 184 ms                                                         | 162 ms: 1.14x faster                                                        |
| scimark_fft                      | 124 ms                                                         | 110 ms: 1.12x faster                                                        |
| fannkuch                         | 179 ms                                                         | 159 ms: 1.12x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 20.7 ms: 1.12x faster                                                       |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.12x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 9.64 ms: 1.12x faster                                                       |
| pidigits                         | 166 ms                                                         | 149 ms: 1.11x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 271 ms: 1.11x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                        |
| richards                         | 22.1 ms                                                        | 20.2 ms: 1.09x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.1 ms: 1.09x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.63 ms: 1.08x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.5 ms: 1.08x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                        |
| telco                            | 3.07 ms                                                        | 2.86 ms: 1.07x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 23.1 ms: 1.07x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 41.4 ms: 1.06x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                       |
| sphinx                           | 409 ms                                                         | 391 ms: 1.04x faster                                                        |
| json                             | 1.94 ms                                                        | 1.86 ms: 1.04x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 95.7 us: 1.04x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.31 ms: 1.04x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 311 ms: 1.04x faster                                                        |
| logging_simple                   | 2.24 us                                                        | 2.17 us: 1.03x faster                                                       |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 92.2 ms: 1.03x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.74 ms: 1.02x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                        |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 637 ms: 1.02x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 931 ns: 1.02x faster                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 7.41 ms: 1.02x faster                                                       |
| logging_format                   | 2.45 us                                                        | 2.41 us: 1.01x faster                                                       |
| deltablue                        | 1.45 ms                                                        | 1.44 ms: 1.01x faster                                                       |
| bench_thread_pool                | 412 us                                                         | 408 us: 1.01x faster                                                        |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 6.78 us: 1.00x faster                                                       |
| pycparser                        | 470 ms                                                         | 474 ms: 1.01x slower                                                        |
| chaos                            | 24.3 ms                                                        | 24.6 ms: 1.01x slower                                                       |
| 2to3                             | 112 ms                                                         | 113 ms: 1.02x slower                                                        |
| meteor_contest                   | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                       |
| raytrace                         | 109 ms                                                         | 112 ms: 1.03x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 99.2 ms: 1.04x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 42.8 ns: 1.05x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.06x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 55.7 ms: 1.06x slower                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 66.8 ms: 1.07x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 45.9 ms: 1.07x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.07x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.47 ms: 1.09x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 36.6 ms: 1.09x slower                                                       |
| generators                       | 15.7 ms                                                        | 17.2 ms: 1.09x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 42.2 ms: 1.12x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 53.7 ms: 1.12x slower                                                       |
| many_optionals                   | 200 us                                                         | 228 us: 1.14x slower                                                        |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 142 ms: 1.38x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.8 ms: 3.24x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                                |

Benchmark hidden because not significant (3): mako, nbody, connected_components
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261119-3.16.0a2+dev-94250a7/bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.103x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.10x