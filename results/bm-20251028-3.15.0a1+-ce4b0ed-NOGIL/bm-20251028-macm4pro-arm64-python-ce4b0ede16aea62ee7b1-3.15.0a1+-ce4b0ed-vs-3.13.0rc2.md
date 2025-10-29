# Results vs. 3.13.0rc2

- fork: python
- ref: ce4b0ede16aea62ee7b1
- machine: darwin-arm64
- commit hash: ce4b0ed
- commit date: 2025-10-28
- overall geometric mean: 1.004x slower
- HPT reliability: 76.31%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 126 ms: 1.13x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                    |
| sphinx         | 409 ms                                                         | 415 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.65x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.53x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 200 ms: 2.03x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 212 ms: 1.82x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 87.7 ms: 1.51x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 238 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.0 ms: 2.73x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 61.3 ms: 1.44x slower                                                    |
| Geometric mean | (ref)                                                          | 1.11x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.33 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 53.8 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.9 ms: 1.22x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.07 ms: 1.14x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 58.7 ms: 1.06x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 968 ms: 1.03x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 37.7 ms: 1.05x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.07x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 154 us: 1.18x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.71 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.07 ms: 1.19x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.7 ms: 1.16x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.9 ms: 1.19x slower                                                    |
| mako            | 4.41 ms                                                        | 5.84 ms: 1.32x slower                                                    |
| django_template | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.25x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.65x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 774 us: 2.64x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.53x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 478 us: 2.08x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 200 ms: 2.03x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 212 ms: 1.82x faster                                                     |
| mdp                              | 1.06 sec                                                       | 610 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 87.7 ms: 1.51x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                     |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.48x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 238 ms: 1.27x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.24x faster                                                    |
| deepcopy                         | 145 us                                                         | 119 us: 1.22x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.9 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                     |
| go                               | 72.6 ms                                                        | 62.5 ms: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.33 ms: 1.15x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.07 ms: 1.14x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 56.0 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 844 ns: 1.12x faster                                                     |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.7 ms: 1.06x faster                                                    |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                     |
| float                            | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.03 sec: 1.05x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 968 ms: 1.03x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.3 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.27 us: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                     |
| sphinx                           | 409 ms                                                         | 415 ms: 1.02x slower                                                     |
| pycparser                        | 470 ms                                                         | 479 ms: 1.02x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                    |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                     |
| json                             | 1.94 ms                                                        | 2.03 ms: 1.05x slower                                                    |
| fannkuch                         | 179 ms                                                         | 188 ms: 1.05x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.7 ms: 1.05x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.07x slower                                                    |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.08 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.1 ms: 1.09x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 136 ms: 1.10x slower                                                     |
| thrift                           | 309 us                                                         | 339 us: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 355 ms: 1.10x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 27.5 ms: 1.11x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 726 ms: 1.12x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 45.5 ns: 1.12x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 53.8 ms: 1.12x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.20 ms: 1.12x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.71 ms: 1.12x slower                                                    |
| 2to3                             | 112 ms                                                         | 126 ms: 1.13x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 42.6 ms: 1.13x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.54 us: 1.14x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.2 ms: 1.14x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.80 us: 1.15x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.67 ms: 1.15x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 74.6 us: 1.15x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 24.7 ms: 1.16x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.2 ms: 1.17x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.3 ms: 1.17x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.18x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 154 us: 1.18x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 44.0 ms: 1.18x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.07 ms: 1.19x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.9 ms: 1.19x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 57.2 ms: 1.19x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 192 ms: 1.20x slower                                                     |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                     |
| generators                       | 15.7 ms                                                        | 19.2 ms: 1.22x slower                                                    |
| chaos                            | 24.3 ms                                                        | 30.0 ms: 1.23x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.58 us: 1.26x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.8 ms: 1.27x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.30 ms: 1.29x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.9 ms: 1.31x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 544 us: 1.32x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.84 ms: 1.32x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 56.8 ms: 1.33x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                    |
| nbody                            | 42.5 ms                                                        | 61.3 ms: 1.44x slower                                                    |
| many_optionals                   | 200 us                                                         | 390 us: 1.95x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.0 ms: 2.73x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 19.3 ms: 3.08x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (3): regex_dna, telco, async_tree_eager_cpu_io_mixed
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251028-3.15.0a1+-ce4b0ed-NOGIL/bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 76.31% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x