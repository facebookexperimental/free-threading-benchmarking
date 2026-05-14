# Results vs. 3.13.0rc2

- fork: python
- ref: f1a47e79fb7081d3cde6
- machine: darwin-arm64
- commit hash: f1a47e7
- commit date: 2026-05-14
- overall geometric mean: 1.068x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 954 ms: 1.10x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.9 ms: 1.06x faster                                                   |
| sphinx         | 409 ms                                                         | 401 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 303 ms: 1.74x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 330 ms: 1.58x faster                                                    |
| async_generators                 | 193 ms                                                         | 145 ms: 1.34x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 304 ms: 1.27x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 323 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 118 ms: 1.21x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 170 ms: 1.09x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.9 ms: 1.08x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 123 ms: 1.08x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 276 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 173 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 286 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 257 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 149 ms: 1.46x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 100 ms: 3.47x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                    |
| nbody          | 42.5 ms                                                        | 43.0 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.12x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.68 ms: 1.11x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 45.1 ms: 1.06x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 93.6 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                          | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 818 ms: 1.22x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.6 ms: 1.08x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 96.3 us: 1.03x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.03x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.07x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 67.6 ms: 1.08x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                   |
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 504 ms: 2.10x faster                                                    |
| pylint                           | 106 ms                                                         | 55.6 ms: 1.90x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 303 ms: 1.74x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 330 ms: 1.58x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.08 ms: 1.53x faster                                                   |
| deepcopy                         | 145 us                                                         | 97.3 us: 1.49x faster                                                   |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.45x faster                                                  |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.41x faster                                                   |
| go                               | 72.6 ms                                                        | 51.6 ms: 1.40x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 48.1 us: 1.34x faster                                                   |
| async_generators                 | 193 ms                                                         | 145 ms: 1.34x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.0 ms: 1.31x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 304 ms: 1.27x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 323 ms: 1.25x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 818 ms: 1.22x faster                                                    |
| pyflate                          | 222 ms                                                         | 182 ms: 1.22x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 118 ms: 1.21x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 850 us: 1.17x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.12x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.68 ms: 1.11x faster                                                   |
| docutils                         | 1.05 sec                                                       | 954 ms: 1.10x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.80 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                  |
| async_tree_memoization_tg        | 186 ms                                                         | 170 ms: 1.09x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.2 ms: 1.09x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 39.9 ms: 1.08x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.6 ms: 1.08x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.7 ms: 1.08x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 123 ms: 1.08x faster                                                    |
| float                            | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.0 ms: 1.07x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.07x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 276 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 173 ms: 1.06x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 45.1 ms: 1.06x faster                                                   |
| fannkuch                         | 179 ms                                                         | 169 ms: 1.06x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.9 ms: 1.06x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 35.2 ms: 1.06x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.94 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 286 ms: 1.05x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.71 ms: 1.05x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.05x faster                                                   |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 624 ms: 1.04x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 310 ms: 1.04x faster                                                    |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.29 ms: 1.03x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 96.3 us: 1.03x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.03x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.39 us: 1.02x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.18 us: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 401 ms: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 931 ns: 1.02x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 43.2 ms: 1.01x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 93.6 ms: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| connected_components             | 208 ms                                                         | 207 ms: 1.00x faster                                                    |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.85 us: 1.01x slower                                                   |
| nbody                            | 42.5 ms                                                        | 43.0 ms: 1.01x slower                                                   |
| pycparser                        | 470 ms                                                         | 476 ms: 1.01x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.0 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                   |
| raytrace                         | 109 ms                                                         | 112 ms: 1.03x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 54.0 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.85 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.5 ms: 1.04x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.07x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 67.6 ms: 1.08x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 46.5 ms: 1.09x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.8 ms: 1.15x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.4 ms: 1.17x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                   |
| many_optionals                   | 200 us                                                         | 239 us: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.1 ms: 1.22x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 257 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 149 ms: 1.46x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 100 ms: 3.47x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (6): dask, xml_etree_generate, logging_silent, thrift, chaos, deltablue
Ignored benchmarks (16) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, asyncio_websockets, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260514-3.16.0a0-f1a47e7/bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.068x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.17x