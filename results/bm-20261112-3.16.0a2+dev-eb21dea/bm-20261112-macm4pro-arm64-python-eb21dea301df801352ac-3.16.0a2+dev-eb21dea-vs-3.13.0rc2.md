# Results vs. 3.13.0rc2

- fork: python
- ref: eb21dea301df801352ac
- machine: darwin-arm64
- commit hash: eb21dea
- commit date: 2026-11-12
- overall geometric mean: 1.103x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                        |
| docutils       | 1.05 sec                                                       | 911 ms: 1.15x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.7 ms: 1.12x faster                                                       |
| sphinx         | 409 ms                                                         | 390 ms: 1.05x faster                                                        |
| Geometric mean | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 267 ms: 1.97x faster                                                        |
| async_generators                 | 193 ms                                                         | 98.4 ms: 1.96x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 279 ms: 1.87x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 278 ms: 1.45x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 273 ms: 1.42x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.18x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 158 ms: 1.18x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.41 ms: 1.14x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 163 ms: 1.13x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 273 ms: 1.10x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.09x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.7 ms: 1.06x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 143 ms: 1.39x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.9 ms: 3.25x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                       |
| pidigits       | 166 ms                                                         | 148 ms: 1.12x faster                                                        |
| nbody          | 42.5 ms                                                        | 40.5 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                          | 1.10x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.27 ms: 1.15x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 91.3 ms: 1.04x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 53.8 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.61 ms: 1.29x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 808 ms: 1.24x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.6 ms: 1.11x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 95.5 us: 1.04x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 64.8 ms: 1.04x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.07x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.09 ms: 1.07x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.00x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 12.5 ms                                                        | 14.8 ms: 1.19x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                                |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 502 ms: 2.11x faster                                                        |
| pylint                           | 106 ms                                                         | 51.1 ms: 2.07x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 267 ms: 1.97x faster                                                        |
| async_generators                 | 193 ms                                                         | 98.4 ms: 1.96x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 279 ms: 1.87x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.99 ms: 1.57x faster                                                       |
| create_gc_cycles                 | 993 us                                                         | 639 us: 1.56x faster                                                        |
| deepcopy                         | 145 us                                                         | 96.1 us: 1.51x faster                                                       |
| k_core                           | 1.46 sec                                                       | 970 ms: 1.51x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 278 ms: 1.45x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 45.4 us: 1.42x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.42x faster                                                       |
| async_tree_io                    | 386 ms                                                         | 273 ms: 1.42x faster                                                        |
| go                               | 72.6 ms                                                        | 52.4 ms: 1.39x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 49.3 ms: 1.30x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.61 ms: 1.29x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.04 us: 1.25x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 808 ms: 1.24x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| pyflate                          | 222 ms                                                         | 183 ms: 1.21x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.18x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 158 ms: 1.18x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.27 ms: 1.15x faster                                                       |
| docutils                         | 1.05 sec                                                       | 911 ms: 1.15x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.41 ms: 1.14x faster                                                       |
| gc_traversal                     | 2.04 ms                                                        | 1.79 ms: 1.14x faster                                                       |
| float                            | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 163 ms: 1.13x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.88 sec: 1.13x faster                                                      |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.4 ms: 1.13x faster                                                       |
| fannkuch                         | 179 ms                                                         | 158 ms: 1.13x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 20.7 ms: 1.12x faster                                                       |
| pidigits                         | 166 ms                                                         | 148 ms: 1.12x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.6 ms: 1.11x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 273 ms: 1.10x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.09x faster                                                        |
| scimark_fft                      | 124 ms                                                         | 114 ms: 1.09x faster                                                        |
| telco                            | 3.07 ms                                                        | 2.82 ms: 1.09x faster                                                       |
| richards                         | 22.1 ms                                                        | 20.3 ms: 1.09x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.63 ms: 1.08x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.5 ms: 1.08x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                        |
| python_startup                   | 8.63 ms                                                        | 8.09 ms: 1.07x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 23.2 ms: 1.06x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 40.7 ms: 1.06x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 41.5 ms: 1.05x faster                                                       |
| nbody                            | 42.5 ms                                                        | 40.5 ms: 1.05x faster                                                       |
| sphinx                           | 409 ms                                                         | 390 ms: 1.05x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 95.5 us: 1.04x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 91.3 ms: 1.04x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 311 ms: 1.03x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 917 ns: 1.03x faster                                                        |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.33 ms: 1.03x faster                                                       |
| comprehensions                   | 6.80 us                                                        | 6.64 us: 1.03x faster                                                       |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.74 ms: 1.02x faster                                                       |
| thrift                           | 309 us                                                         | 302 us: 1.02x faster                                                        |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.20 us: 1.02x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.02x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.44 ms: 1.01x faster                                                       |
| logging_format                   | 2.45 us                                                        | 2.42 us: 1.01x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 645 ms: 1.01x faster                                                        |
| bench_thread_pool                | 412 us                                                         | 409 us: 1.01x faster                                                        |
| connected_components             | 208 ms                                                         | 207 ms: 1.01x faster                                                        |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.00x faster                                                        |
| chaos                            | 24.3 ms                                                        | 24.7 ms: 1.02x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                       |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                        |
| logging_silent                   | 40.6 ns                                                        | 41.9 ns: 1.03x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 99.0 ms: 1.04x slower                                                       |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 64.8 ms: 1.04x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 55.0 ms: 1.05x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.07x slower                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 36.6 ms: 1.09x slower                                                       |
| generators                       | 15.7 ms                                                        | 17.1 ms: 1.09x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 46.6 ms: 1.09x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 53.8 ms: 1.12x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 42.5 ms: 1.12x slower                                                       |
| many_optionals                   | 200 us                                                         | 233 us: 1.16x slower                                                        |
| django_template                  | 12.5 ms                                                        | 14.8 ms: 1.19x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 143 ms: 1.39x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.9 ms: 3.25x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                                |

Benchmark hidden because not significant (2): mako, pycparser
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261112-3.16.0a2+dev-eb21dea/bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.103x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.10x