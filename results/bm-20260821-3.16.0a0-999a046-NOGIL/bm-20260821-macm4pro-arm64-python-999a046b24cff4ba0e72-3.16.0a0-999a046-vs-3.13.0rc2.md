# Results vs. 3.13.0rc2

- fork: python
- ref: 999a046b24cff4ba0e72
- machine: darwin-arm64
- commit hash: 999a046
- commit date: 2026-08-21
- overall geometric mean: 1.060x slower
- HPT reliability: 99.65%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 136 ms: 1.22x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.10 sec: 1.05x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.2 ms: 1.04x slower                                                   |
| sphinx         | 409 ms                                                         | 461 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                          | 1.11x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 307 ms: 1.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 312 ms: 1.68x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 313 ms: 1.30x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 318 ms: 1.22x faster                                                    |
| async_generators                 | 193 ms                                                         | 164 ms: 1.18x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 191 ms: 1.04x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 148 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 307 ms: 1.05x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 128 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 238 ms: 1.06x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 147 ms: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 52.0 ms: 1.20x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 13.7 ms: 1.28x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 280 ms: 1.35x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 159 ms: 1.55x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.12x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| float          | 31.4 ms                                                        | 35.3 ms: 1.12x slower                                                   |
| nbody          | 42.5 ms                                                        | 62.0 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                          | 1.18x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.06 ms: 1.18x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.5 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 68.7 ms: 1.43x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.80 ms: 1.22x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.5 ms: 1.11x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.2 ms: 1.07x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 946 ms: 1.06x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.02x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 39.3 ms: 1.10x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 116 us: 1.17x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 31.4 ms: 1.24x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 164 us: 1.26x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.23 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.79 ms: 1.31x slower                                                   |
| django_template | 12.5 ms                                                        | 17.7 ms: 1.42x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.36x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 779 us: 2.62x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 487 us: 2.04x faster                                                    |
| pylint                           | 106 ms                                                         | 54.5 ms: 1.94x faster                                                   |
| mdp                              | 1.06 sec                                                       | 618 ms: 1.71x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 307 ms: 1.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 312 ms: 1.68x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.45x faster                                                  |
| subparsers                       | 6.26 ms                                                        | 4.55 ms: 1.38x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 313 ms: 1.30x faster                                                    |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.80 ms: 1.22x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 318 ms: 1.22x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.06 ms: 1.18x faster                                                   |
| async_generators                 | 193 ms                                                         | 164 ms: 1.18x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 814 ns: 1.16x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.5 ms: 1.11x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 15.0 us: 1.09x faster                                                   |
| go                               | 72.6 ms                                                        | 66.4 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 58.2 ms: 1.07x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 60.3 us: 1.07x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 946 ms: 1.06x faster                                                    |
| pyflate                          | 222 ms                                                         | 212 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 61.4 ms: 1.04x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.04x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 92.5 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.02x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.15 ms: 1.03x slower                                                   |
| async_tree_memoization           | 184 ms                                                         | 191 ms: 1.04x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 148 ms: 1.04x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.2 ms: 1.04x slower                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 307 ms: 1.05x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 128 ms: 1.05x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.10 sec: 1.05x slower                                                  |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 238 ms: 1.06x slower                                                    |
| fannkuch                         | 179 ms                                                         | 190 ms: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 512 ms: 1.09x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 135 ms: 1.09x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 39.3 ms: 1.10x slower                                                   |
| async_tree_none_tg               | 133 ms                                                         | 147 ms: 1.11x slower                                                    |
| float                            | 31.4 ms                                                        | 35.3 ms: 1.12x slower                                                   |
| sphinx                           | 409 ms                                                         | 461 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                   |
| shortest_path                    | 225 ms                                                         | 255 ms: 1.14x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.56 ms: 1.14x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 368 ms: 1.14x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.0 ms: 1.16x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 756 ms: 1.16x slower                                                    |
| thrift                           | 309 us                                                         | 360 us: 1.17x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 116 us: 1.17x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.62 us: 1.17x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.87 us: 1.17x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 35.3 ms: 1.18x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 43.9 ms: 1.18x slower                                                   |
| connected_components             | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 52.0 ms: 1.20x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 115 ms: 1.21x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 63.1 ms: 1.21x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.23 ms: 1.21x slower                                                   |
| 2to3                             | 112 ms                                                         | 136 ms: 1.22x slower                                                    |
| richards                         | 22.1 ms                                                        | 27.1 ms: 1.23x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 196 ms: 1.23x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.19 ms: 1.23x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 30.6 ms: 1.24x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 31.4 ms: 1.24x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 54.3 ms: 1.24x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.54 ms: 1.24x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.3 ms: 1.26x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 164 us: 1.26x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 51.2 ns: 1.26x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 13.7 ms: 1.28x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.71 us: 1.28x slower                                                   |
| chaos                            | 24.3 ms                                                        | 31.6 ms: 1.30x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.79 ms: 1.31x slower                                                   |
| coverage                         | 31.2 ms                                                        | 41.4 ms: 1.33x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 280 ms: 1.35x slower                                                    |
| many_optionals                   | 200 us                                                         | 272 us: 1.36x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 577 us: 1.40x slower                                                    |
| django_template                  | 12.5 ms                                                        | 17.7 ms: 1.42x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 68.7 ms: 1.43x slower                                                   |
| raytrace                         | 109 ms                                                         | 158 ms: 1.45x slower                                                    |
| nbody                            | 42.5 ms                                                        | 62.0 ms: 1.46x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 2.22 ms: 1.53x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 159 ms: 1.55x slower                                                    |
| generators                       | 15.7 ms                                                        | 24.8 ms: 1.58x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 72.1 ms: 1.69x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.12x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (4): dulwich_log, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, json
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260821-3.16.0a0-999a046-NOGIL/bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.060x slower

# HPT report

- Reliability score: 99.65% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.24x