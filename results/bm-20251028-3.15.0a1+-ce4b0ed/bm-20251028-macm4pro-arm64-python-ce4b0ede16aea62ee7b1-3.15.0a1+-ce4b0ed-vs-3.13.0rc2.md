# Results vs. 3.13.0rc2

- fork: python
- ref: ce4b0ede16aea62ee7b1
- machine: darwin-arm64
- commit hash: ce4b0ed
- commit date: 2025-10-28
- overall geometric mean: 1.028x faster
- HPT reliability: 94.09%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| html5lib       | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                    |
| sphinx         | 409 ms                                                         | 404 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 228 ms: 2.28x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 230 ms: 2.28x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 230 ms: 1.68x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 142 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.4 ms: 2.85x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.18x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 50.4 ms: 1.19x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.88 ms: 1.08x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 49.7 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.8 ms: 1.16x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 910 ms: 1.10x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 61.0 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.02x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.28 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.9 ms: 1.03x slower                                                    |
| mako            | 4.41 ms                                                        | 4.86 ms: 1.10x slower                                                    |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 228 ms: 2.28x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 230 ms: 2.28x faster                                                     |
| mdp                              | 1.06 sec                                                       | 540 ms: 1.96x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 230 ms: 1.68x faster                                                     |
| k_core                           | 1.46 sec                                                       | 901 ms: 1.62x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.3 us: 1.34x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 48.7 ms: 1.31x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 142 ms: 1.30x faster                                                     |
| go                               | 72.6 ms                                                        | 56.4 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.8 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 910 ms: 1.10x faster                                                     |
| float                            | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.88 ms: 1.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 935 us: 1.06x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.94 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| richards                         | 22.1 ms                                                        | 21.4 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.0 ms: 1.02x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.4 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| connected_components             | 208 ms                                                         | 204 ms: 1.02x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 24.3 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.5 ms: 1.01x faster                                                    |
| sphinx                           | 409 ms                                                         | 404 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.55 ms: 1.00x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 2.86 ms: 1.00x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                    |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 418 us: 1.01x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 327 ms: 1.02x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 661 ms: 1.02x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.02x slower                                                     |
| thrift                           | 309 us                                                         | 316 us: 1.02x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.9 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 66.4 us: 1.03x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                    |
| pycparser                        | 470 ms                                                         | 483 ms: 1.03x slower                                                     |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 41.7 ns: 1.03x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.2 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.6 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.84 ms: 1.04x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.7 ms: 1.04x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 985 ns: 1.04x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.34 us: 1.05x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.57 us: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.28 ms: 1.06x slower                                                    |
| fannkuch                         | 179 ms                                                         | 189 ms: 1.06x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 39.9 ms: 1.07x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                     |
| chaos                            | 24.3 ms                                                        | 26.3 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 57.1 ms: 1.09x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 41.3 ms: 1.09x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.48 us: 1.10x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.86 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.12x slower                                                    |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 48.2 ms: 1.13x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.2 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| nbody                            | 42.5 ms                                                        | 50.4 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| many_optionals                   | 200 us                                                         | 369 us: 1.84x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.4 ms: 2.85x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.0 ms: 2.87x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (5): docutils, genshi_text, regex_dna, spectral_norm, scimark_fft
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251028-3.15.0a1+-ce4b0ed/bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.028x faster

# HPT report

- Reliability score: 94.09% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.16x