# Results vs. 3.13.0rc2

- fork: python
- ref: ecefd40671f340d543c2
- machine: darwin-arm64
- commit hash: ecefd40
- commit date: 2026-11-12
- overall geometric mean: 1.017x slower
- HPT reliability: 95.67%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 128 ms: 1.14x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                      |
| html5lib       | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                       |
| sphinx         | 409 ms                                                         | 453 ms: 1.11x slower                                                        |
| Geometric mean | (ref)                                                          | 1.06x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 302 ms: 1.72x faster                                                        |
| async_generators                 | 193 ms                                                         | 113 ms: 1.71x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 307 ms: 1.71x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 305 ms: 1.33x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 306 ms: 1.26x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 294 ms: 1.03x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 300 ms: 1.02x slower                                                        |
| async_tree_none                  | 142 ms                                                         | 146 ms: 1.02x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 232 ms: 1.03x slower                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 126 ms: 1.03x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 143 ms: 1.08x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 11.8 ms: 1.10x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 273 ms: 1.31x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 157 ms: 1.53x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 116 ms: 4.00x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                                |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 151 ms: 1.10x faster                                                        |
| float          | 31.4 ms                                                        | 33.2 ms: 1.06x slower                                                       |
| nbody          | 42.5 ms                                                        | 59.7 ms: 1.40x slower                                                       |
| Geometric mean | (ref)                                                          | 1.11x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.26 ms: 1.16x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 93.9 ms: 1.01x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 64.2 ms: 1.34x slower                                                       |
| Geometric mean | (ref)                                                          | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.77 ms: 1.23x faster                                                       |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.6 ms: 1.11x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 904 ms: 1.11x faster                                                        |
| xml_etree_parse      | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                       |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.03x slower                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 38.0 ms: 1.06x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.09x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.4 ms: 1.16x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 158 us: 1.22x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.88 ms: 1.03x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.92 ms: 1.16x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.09x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.56 ms: 1.26x slower                                                       |
| django_template | 12.5 ms                                                        | 16.8 ms: 1.35x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.30x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 794 us: 2.57x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 473 us: 2.10x faster                                                        |
| pylint                           | 106 ms                                                         | 52.6 ms: 2.01x faster                                                       |
| mdp                              | 1.06 sec                                                       | 591 ms: 1.79x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 302 ms: 1.72x faster                                                        |
| async_generators                 | 193 ms                                                         | 113 ms: 1.71x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 307 ms: 1.71x faster                                                        |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                      |
| subparsers                       | 6.26 ms                                                        | 4.30 ms: 1.46x faster                                                       |
| async_tree_io_tg                 | 405 ms                                                         | 305 ms: 1.33x faster                                                        |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 306 ms: 1.26x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.77 ms: 1.23x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 53.8 us: 1.20x faster                                                       |
| go                               | 72.6 ms                                                        | 60.4 ms: 1.20x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 9.26 ms: 1.16x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 823 ns: 1.15x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.88 sec: 1.13x faster                                                      |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.6 ms: 1.11x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 904 ms: 1.11x faster                                                        |
| pidigits                         | 166 ms                                                         | 151 ms: 1.10x faster                                                        |
| scimark_sor                      | 64.0 ms                                                        | 58.4 ms: 1.10x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 15.3 us: 1.07x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.21 us: 1.07x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 294 ms: 1.03x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 93.9 ms: 1.01x faster                                                       |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                      |
| html5lib                         | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                       |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                       |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.02x slower                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 300 ms: 1.02x slower                                                        |
| async_tree_none                  | 142 ms                                                         | 146 ms: 1.02x slower                                                        |
| python_startup                   | 8.63 ms                                                        | 8.88 ms: 1.03x slower                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 232 ms: 1.03x slower                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 126 ms: 1.03x slower                                                        |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.03x slower                                                       |
| pycparser                        | 470 ms                                                         | 492 ms: 1.05x slower                                                        |
| float                            | 31.4 ms                                                        | 33.2 ms: 1.06x slower                                                       |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 38.0 ms: 1.06x slower                                                       |
| async_tree_none_tg               | 133 ms                                                         | 143 ms: 1.08x slower                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 8.18 ms: 1.09x slower                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.09x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 11.8 ms: 1.10x slower                                                       |
| richards                         | 22.1 ms                                                        | 24.2 ms: 1.10x slower                                                       |
| logging_simple                   | 2.24 us                                                        | 2.46 us: 1.10x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 41.8 ms: 1.11x slower                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 356 ms: 1.11x slower                                                        |
| sphinx                           | 409 ms                                                         | 453 ms: 1.11x slower                                                        |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                       |
| shortest_path                    | 225 ms                                                         | 250 ms: 1.11x slower                                                        |
| logging_format                   | 2.45 us                                                        | 2.73 us: 1.11x slower                                                       |
| thrift                           | 309 us                                                         | 346 us: 1.12x slower                                                        |
| richards_super                   | 24.7 ms                                                        | 27.7 ms: 1.12x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 53.9 ms: 1.12x slower                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                       |
| spectral_norm                    | 43.7 ms                                                        | 49.7 ms: 1.14x slower                                                       |
| bench_thread_pool                | 412 us                                                         | 470 us: 1.14x slower                                                        |
| 2to3                             | 112 ms                                                         | 128 ms: 1.14x slower                                                        |
| pprint_pformat                   | 650 ms                                                         | 748 ms: 1.15x slower                                                        |
| connected_components             | 208 ms                                                         | 240 ms: 1.16x slower                                                        |
| xml_etree_process                | 25.4 ms                                                        | 29.4 ms: 1.16x slower                                                       |
| nqueens                          | 37.2 ms                                                        | 43.2 ms: 1.16x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.92 ms: 1.16x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 61.9 ms: 1.18x slower                                                       |
| chaos                            | 24.3 ms                                                        | 28.7 ms: 1.18x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.15 ms: 1.21x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 49.2 ns: 1.21x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 158 us: 1.22x slower                                                        |
| comprehensions                   | 6.80 us                                                        | 8.29 us: 1.22x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 41.4 ms: 1.23x slower                                                       |
| deltablue                        | 1.45 ms                                                        | 1.79 ms: 1.24x slower                                                       |
| raytrace                         | 109 ms                                                         | 137 ms: 1.26x slower                                                        |
| mako                             | 4.41 ms                                                        | 5.56 ms: 1.26x slower                                                       |
| many_optionals                   | 200 us                                                         | 257 us: 1.28x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 273 ms: 1.31x slower                                                        |
| coverage                         | 31.2 ms                                                        | 41.1 ms: 1.32x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 64.2 ms: 1.34x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.8 ms: 1.35x slower                                                       |
| nbody                            | 42.5 ms                                                        | 59.7 ms: 1.40x slower                                                       |
| generators                       | 15.7 ms                                                        | 23.8 ms: 1.52x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 157 ms: 1.53x slower                                                        |
| scimark_lu                       | 42.8 ms                                                        | 66.5 ms: 1.55x slower                                                       |
| async_tree_eager_tg              | 28.9 ms                                                        | 116 ms: 4.00x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                                |

Benchmark hidden because not significant (4): async_tree_memoization_tg, telco, dulwich_log, async_tree_memoization
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261112-3.16.0a2+dev-ecefd40-NOGIL/bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.017x slower

# HPT report

- Reliability score: 95.67% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.19x