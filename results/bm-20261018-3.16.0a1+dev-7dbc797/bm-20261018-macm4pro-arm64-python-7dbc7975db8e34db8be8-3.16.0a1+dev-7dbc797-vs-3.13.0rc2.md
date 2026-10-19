# Results vs. 3.13.0rc2

- fork: python
- ref: 7dbc7975db8e34db8be8
- machine: darwin-arm64
- commit hash: 7dbc797
- commit date: 2026-10-18
- overall geometric mean: 1.100x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.03x slower                                                        |
| docutils       | 1.05 sec                                                       | 901 ms: 1.16x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.6 ms: 1.12x faster                                                       |
| sphinx         | 409 ms                                                         | 387 ms: 1.05x faster                                                        |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 264 ms: 1.99x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 278 ms: 1.88x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 279 ms: 1.45x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 271 ms: 1.42x faster                                                        |
| async_generators                 | 193 ms                                                         | 142 ms: 1.36x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.18x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 157 ms: 1.18x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 161 ms: 1.15x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.73 ms: 1.11x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 273 ms: 1.11x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.8 ms: 1.06x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.3 ms: 3.23x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.5 ms: 1.14x faster                                                       |
| pidigits       | 166 ms                                                         | 160 ms: 1.03x faster                                                        |
| nbody          | 42.5 ms                                                        | 42.3 ms: 1.00x faster                                                       |
| Geometric mean | (ref)                                                          | 1.06x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.57 ms: 1.12x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 54.0 ms: 1.13x slower                                                       |
| Geometric mean | (ref)                                                          | 1.05x faster                                                                |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.55 ms: 1.31x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 823 ms: 1.22x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.4 ms: 1.11x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 92.9 us: 1.07x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.3 us: 1.05x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 63.7 ms: 1.02x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 137 us: 1.05x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.74 ms: 1.01x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.39 ms: 1.07x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.47 ms: 1.01x slower                                                       |
| django_template | 12.5 ms                                                        | 14.8 ms: 1.19x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 501 ms: 2.11x faster                                                        |
| pylint                           | 106 ms                                                         | 51.9 ms: 2.03x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 264 ms: 1.99x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 278 ms: 1.88x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 627 us: 1.58x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.97 ms: 1.58x faster                                                       |
| deepcopy                         | 145 us                                                         | 95.9 us: 1.51x faster                                                       |
| k_core                           | 1.46 sec                                                       | 971 ms: 1.51x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 279 ms: 1.45x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 271 ms: 1.42x faster                                                        |
| go                               | 72.6 ms                                                        | 51.5 ms: 1.41x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.39x faster                                                       |
| async_generators                 | 193 ms                                                         | 142 ms: 1.36x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 48.5 us: 1.33x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.55 ms: 1.31x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 49.4 ms: 1.29x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.25x faster                                                       |
| pyflate                          | 222 ms                                                         | 181 ms: 1.23x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 823 ms: 1.22x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.18x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 157 ms: 1.18x faster                                                        |
| docutils                         | 1.05 sec                                                       | 901 ms: 1.16x faster                                                        |
| gc_traversal                     | 2.04 ms                                                        | 1.76 ms: 1.16x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 161 ms: 1.15x faster                                                        |
| float                            | 31.4 ms                                                        | 27.5 ms: 1.14x faster                                                       |
| fannkuch                         | 179 ms                                                         | 157 ms: 1.13x faster                                                        |
| scimark_fft                      | 124 ms                                                         | 110 ms: 1.13x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 20.6 ms: 1.12x faster                                                       |
| dulwich_log                      | 19.8 ms                                                        | 17.7 ms: 1.12x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 9.57 ms: 1.12x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.12x faster                                                      |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.8 ms: 1.12x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.4 ms: 1.11x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 9.73 ms: 1.11x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 273 ms: 1.11x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                        |
| richards                         | 22.1 ms                                                        | 20.2 ms: 1.09x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.60 ms: 1.09x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                        |
| nqueens                          | 37.2 ms                                                        | 34.4 ms: 1.08x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 22.9 ms: 1.08x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 92.9 us: 1.07x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 41.3 ms: 1.06x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 40.8 ms: 1.06x faster                                                       |
| json                             | 1.94 ms                                                        | 1.84 ms: 1.06x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.12 us: 1.06x faster                                                       |
| sphinx                           | 409 ms                                                         | 387 ms: 1.05x faster                                                        |
| telco                            | 3.07 ms                                                        | 2.91 ms: 1.05x faster                                                       |
| json_loads                       | 10.8 us                                                        | 10.3 us: 1.05x faster                                                       |
| logging_format                   | 2.45 us                                                        | 2.33 us: 1.05x faster                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.26 ms: 1.04x faster                                                       |
| comprehensions                   | 6.80 us                                                        | 6.57 us: 1.04x faster                                                       |
| pidigits                         | 166 ms                                                         | 160 ms: 1.03x faster                                                        |
| pprint_safe_repr                 | 322 ms                                                         | 311 ms: 1.03x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 923 ns: 1.03x faster                                                        |
| pprint_pformat                   | 650 ms                                                         | 634 ms: 1.02x faster                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.74 ms: 1.02x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                        |
| thrift                           | 309 us                                                         | 304 us: 1.02x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.43 ms: 1.02x faster                                                       |
| bench_thread_pool                | 412 us                                                         | 407 us: 1.01x faster                                                        |
| nbody                            | 42.5 ms                                                        | 42.3 ms: 1.00x faster                                                       |
| connected_components             | 208 ms                                                         | 207 ms: 1.00x faster                                                        |
| shortest_path                    | 225 ms                                                         | 225 ms: 1.00x slower                                                        |
| meteor_contest                   | 47.9 ms                                                        | 48.2 ms: 1.01x slower                                                       |
| chaos                            | 24.3 ms                                                        | 24.5 ms: 1.01x slower                                                       |
| mako                             | 4.41 ms                                                        | 4.47 ms: 1.01x slower                                                       |
| python_startup                   | 8.63 ms                                                        | 8.74 ms: 1.01x slower                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 63.7 ms: 1.02x slower                                                       |
| 2to3                             | 112 ms                                                         | 114 ms: 1.03x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 98.0 ms: 1.03x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 41.9 ns: 1.03x slower                                                       |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 54.5 ms: 1.04x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                        |
| pickle_pure_python               | 130 us                                                         | 137 us: 1.05x slower                                                        |
| generators                       | 15.7 ms                                                        | 16.8 ms: 1.07x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.39 ms: 1.07x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 36.6 ms: 1.09x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 46.9 ms: 1.10x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 54.0 ms: 1.13x slower                                                       |
| many_optionals                   | 200 us                                                         | 227 us: 1.13x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 43.1 ms: 1.14x slower                                                       |
| django_template                  | 12.5 ms                                                        | 14.8 ms: 1.19x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.3 ms: 3.23x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                                |

Benchmark hidden because not significant (2): pycparser, regex_dna
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261018-3.16.0a1+dev-7dbc797/bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.13x