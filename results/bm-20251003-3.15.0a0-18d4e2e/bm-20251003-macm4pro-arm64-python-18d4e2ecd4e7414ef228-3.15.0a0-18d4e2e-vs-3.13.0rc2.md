# Results vs. 3.13.0rc2

- fork: python
- ref: 18d4e2ecd4e7414ef228
- machine: darwin-arm64
- commit hash: 18d4e2e
- commit date: 2025-10-03
- overall geometric mean: 1.001x slower
- HPT reliability: 72.49%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.04x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.07 sec: 1.02x slower                                                  |
| html5lib       | 23.1 ms                                                        | 25.0 ms: 1.08x slower                                                   |
| sphinx         | 409 ms                                                         | 419 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 257 ms: 2.05x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 258 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 257 ms: 1.58x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.22x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.22x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 152 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 43.0 ms: 1.00x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 90.0 ms: 3.11x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 31.8 ms: 1.01x slower                                                   |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| nbody          | 42.5 ms                                                        | 51.5 ms: 1.21x slower                                                   |
| Geometric mean | (ref)                                                          | 1.08x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 98.1 ms: 1.04x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 50.5 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.92 ms: 1.19x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.1 ms: 1.05x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 957 ms: 1.04x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.8 ms: 1.02x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.9 ms: 1.02x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 104 us: 1.04x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.79 ms: 1.02x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.5 ms: 1.05x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 22.6 ms: 1.06x slower                                                   |
| mako            | 4.41 ms                                                        | 5.11 ms: 1.16x slower                                                   |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 257 ms: 2.05x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 258 ms: 2.02x faster                                                    |
| mdp                              | 1.06 sec                                                       | 555 ms: 1.91x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 257 ms: 1.58x faster                                                    |
| k_core                           | 1.46 sec                                                       | 967 ms: 1.51x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.29x faster                                                   |
| deepcopy                         | 145 us                                                         | 113 us: 1.29x faster                                                    |
| go                               | 72.6 ms                                                        | 58.2 ms: 1.25x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.22x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.22x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 152 ms: 1.22x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 53.1 ms: 1.20x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.92 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| pyflate                          | 222 ms                                                         | 203 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.19 us: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                  |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.90 ms: 1.06x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 940 us: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.1 ms: 1.05x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 957 ms: 1.04x faster                                                    |
| shortest_path                    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| connected_components             | 208 ms                                                         | 203 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 43.0 ms: 1.00x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| richards                         | 22.1 ms                                                        | 22.2 ms: 1.01x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.58 ms: 1.01x slower                                                   |
| float                            | 31.4 ms                                                        | 31.8 ms: 1.01x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 961 ns: 1.01x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.1 ms: 1.02x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.79 ms: 1.02x slower                                                   |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 2.90 ms: 1.02x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.07 sec: 1.02x slower                                                  |
| spectral_norm                    | 43.7 ms                                                        | 44.7 ms: 1.02x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 63.8 ms: 1.02x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.9 ms: 1.02x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 422 us: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 419 ms: 1.03x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.8 ms: 1.03x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 41.9 ns: 1.03x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.11 ms: 1.03x slower                                                   |
| 2to3                             | 112 ms                                                         | 115 ms: 1.04x slower                                                    |
| thrift                           | 309 us                                                         | 320 us: 1.04x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 98.1 ms: 1.04x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.85 ms: 1.04x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 676 ms: 1.04x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 335 ms: 1.04x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 104 us: 1.04x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.5 ms: 1.05x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 50.5 ms: 1.05x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 22.6 ms: 1.06x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 39.5 ms: 1.06x slower                                                   |
| fannkuch                         | 179 ms                                                         | 189 ms: 1.06x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.9 ms: 1.06x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.2 ms: 1.06x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.06x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.40 us: 1.07x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.63 us: 1.08x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 25.0 ms: 1.08x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 173 ms: 1.08x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.58 ms: 1.09x slower                                                   |
| pycparser                        | 470 ms                                                         | 511 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.09x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 57.3 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 42.4 ms: 1.12x slower                                                   |
| raytrace                         | 109 ms                                                         | 122 ms: 1.12x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.3 ms: 1.13x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.9 ms: 1.13x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.74 us: 1.14x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.8 ms: 1.14x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.1 ms: 1.15x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.11 ms: 1.16x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                    |
| nbody                            | 42.5 ms                                                        | 51.5 ms: 1.21x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                    |
| many_optionals                   | 200 us                                                         | 332 us: 1.65x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.4 ms: 2.94x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 90.0 ms: 3.11x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (3): typing_runtime_protocols, async_tree_eager_cpu_io_mixed, json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251003-3.15.0a0-18d4e2e/bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 72.49% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x