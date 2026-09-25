# Results vs. 3.13.0rc2

- fork: python
- ref: 80f9aa0b18d96509eec3
- machine: darwin-arm64
- commit hash: 80f9aa0
- commit date: 2026-09-25
- overall geometric mean: 1.048x faster
- HPT reliability: 98.34%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.07x slower                                                    |
| docutils       | 1.05 sec                                                       | 947 ms: 1.11x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.5 ms: 1.07x faster                                                   |
| sphinx         | 409 ms                                                         | 398 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 342 ms: 1.54x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 340 ms: 1.53x faster                                                    |
| async_generators                 | 193 ms                                                         | 143 ms: 1.35x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 328 ms: 1.24x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 341 ms: 1.13x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.57 ms: 1.12x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 174 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 126 ms: 1.06x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 136 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 285 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 294 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 134 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 250 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 266 ms: 1.28x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 64.7 ms: 1.50x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 155 ms: 1.51x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 104 ms: 3.58x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x slower                                                            |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                   |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 44.4 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.34 ms: 1.15x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 93.6 ms: 1.01x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 53.6 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.57 ms: 1.30x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 791 ms: 1.26x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.0 ms: 1.07x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 97.7 us: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.06x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 67.9 ms: 1.09x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.24 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.72 ms: 1.13x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.10x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.62 ms: 1.05x slower                                                   |
| django_template | 12.5 ms                                                        | 14.8 ms: 1.19x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.12x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 513 ms: 2.06x faster                                                    |
| pylint                           | 106 ms                                                         | 56.0 ms: 1.88x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 342 ms: 1.54x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 340 ms: 1.53x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.11 ms: 1.52x faster                                                   |
| deepcopy                         | 145 us                                                         | 95.9 us: 1.51x faster                                                   |
| k_core                           | 1.46 sec                                                       | 987 ms: 1.48x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.40x faster                                                   |
| go                               | 72.6 ms                                                        | 52.3 ms: 1.39x faster                                                   |
| async_generators                 | 193 ms                                                         | 143 ms: 1.35x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 49.2 us: 1.31x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.1 ms: 1.30x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.57 ms: 1.30x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 791 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 328 ms: 1.24x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                   |
| pyflate                          | 222 ms                                                         | 182 ms: 1.22x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 847 us: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.34 ms: 1.15x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 341 ms: 1.13x faster                                                    |
| fannkuch                         | 179 ms                                                         | 158 ms: 1.13x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.57 ms: 1.12x faster                                                   |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                   |
| docutils                         | 1.05 sec                                                       | 947 ms: 1.11x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.0 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| richards_super                   | 24.7 ms                                                        | 22.7 ms: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.08x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.7 ms: 1.08x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.64 ms: 1.08x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.5 ms: 1.07x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.0 ms: 1.07x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 174 ms: 1.07x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 302 ms: 1.07x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 34.9 ms: 1.07x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.89 ms: 1.06x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 126 ms: 1.06x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 118 ms: 1.05x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 620 ms: 1.05x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 136 ms: 1.05x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.97 ms: 1.04x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.17 us: 1.03x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 42.4 ms: 1.03x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 285 ms: 1.03x faster                                                    |
| sphinx                           | 409 ms                                                         | 398 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 294 ms: 1.03x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 924 ns: 1.03x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.39 us: 1.03x faster                                                   |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.67 us: 1.02x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 97.7 us: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.44 ms: 1.01x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 93.6 ms: 1.01x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| bench_thread_pool                | 412 us                                                         | 415 us: 1.01x slower                                                    |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                   |
| connected_components             | 208 ms                                                         | 210 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.80 ms: 1.01x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 41.2 ns: 1.01x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.0 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 489 ms: 1.04x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.3 ms: 1.04x slower                                                   |
| nbody                            | 42.5 ms                                                        | 44.4 ms: 1.05x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.62 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.3 ms: 1.06x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.06x slower                                                    |
| raytrace                         | 109 ms                                                         | 116 ms: 1.07x slower                                                    |
| 2to3                             | 112 ms                                                         | 119 ms: 1.07x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.24 ms: 1.07x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.1 ms: 1.09x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 67.9 ms: 1.09x slower                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 134 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 250 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.12x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.6 ms: 1.12x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.72 ms: 1.13x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.8 ms: 1.14x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.8 ms: 1.19x slower                                                   |
| many_optionals                   | 200 us                                                         | 244 us: 1.22x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.6 ms: 1.26x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 266 ms: 1.28x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 64.7 ms: 1.50x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 155 ms: 1.51x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 104 ms: 3.58x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (4): json_loads, async_tree_memoization, thrift, shortest_path
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260925-3.16.0a0-80f9aa0/bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.048x faster

# HPT report

- Reliability score: 98.34% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.17x