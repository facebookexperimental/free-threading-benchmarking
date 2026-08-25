# Results vs. 3.13.0rc2

- fork: python
- ref: ee521e8ac19ad012ebc4
- machine: darwin-arm64
- commit hash: ee521e8
- commit date: 2026-08-24
- overall geometric mean: 1.060x faster
- HPT reliability: 99.92%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| docutils       | 1.05 sec                                                       | 938 ms: 1.12x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                   |
| sphinx         | 409 ms                                                         | 402 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 309 ms: 1.70x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 334 ms: 1.56x faster                                                    |
| async_generators                 | 193 ms                                                         | 145 ms: 1.33x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 314 ms: 1.23x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 330 ms: 1.23x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 121 ms: 1.18x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.56 ms: 1.12x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 280 ms: 1.05x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.2 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 289 ms: 1.04x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 177 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 260 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 153 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.56x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| nbody          | 42.5 ms                                                        | 40.6 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.1 ms: 1.03x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 54.1 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.60 ms: 1.29x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 801 ms: 1.25x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.5 ms: 1.06x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.5 us: 1.01x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.08x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 68.4 ms: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.11 ms: 1.06x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.63 ms: 1.11x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.62 ms: 1.05x slower                                                   |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 517 ms: 2.05x faster                                                    |
| pylint                           | 106 ms                                                         | 56.3 ms: 1.87x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 309 ms: 1.70x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 334 ms: 1.56x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.06 ms: 1.54x faster                                                   |
| deepcopy                         | 145 us                                                         | 96.8 us: 1.50x faster                                                   |
| k_core                           | 1.46 sec                                                       | 981 ms: 1.49x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.43x faster                                                   |
| go                               | 72.6 ms                                                        | 52.9 ms: 1.37x faster                                                   |
| async_generators                 | 193 ms                                                         | 145 ms: 1.33x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 48.6 ms: 1.32x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 49.9 us: 1.30x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.60 ms: 1.29x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 801 ms: 1.25x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 314 ms: 1.23x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 330 ms: 1.23x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.22x faster                                                   |
| pyflate                          | 222 ms                                                         | 182 ms: 1.22x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 817 us: 1.22x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 121 ms: 1.18x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.56 ms: 1.12x faster                                                   |
| docutils                         | 1.05 sec                                                       | 938 ms: 1.12x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.09x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.2 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| fannkuch                         | 179 ms                                                         | 164 ms: 1.09x faster                                                    |
| float                            | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 114 ms: 1.08x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.07x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.9 ms: 1.07x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.91 ms: 1.07x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.2 ms: 1.07x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.5 ms: 1.06x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.69 ms: 1.06x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.90 ms: 1.06x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.05x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 41.6 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 280 ms: 1.05x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.2 ms: 1.05x faster                                                   |
| nbody                            | 42.5 ms                                                        | 40.6 ms: 1.05x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 35.6 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 289 ms: 1.04x faster                                                    |
| json                             | 1.94 ms                                                        | 1.86 ms: 1.04x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 177 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 311 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 92.1 ms: 1.03x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.18 us: 1.03x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 924 ns: 1.03x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 637 ms: 1.02x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.40 us: 1.02x faster                                                   |
| sphinx                           | 409 ms                                                         | 402 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| comprehensions                   | 6.80 us                                                        | 6.72 us: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.44 ms: 1.01x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 98.5 us: 1.01x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.3 ms: 1.01x slower                                                   |
| connected_components             | 208 ms                                                         | 210 ms: 1.01x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 423 us: 1.03x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.03x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.0 ns: 1.03x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.1 ms: 1.04x slower                                                   |
| thrift                           | 309 us                                                         | 322 us: 1.04x slower                                                    |
| pycparser                        | 470 ms                                                         | 490 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.5 ms: 1.04x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.62 ms: 1.05x slower                                                   |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.11 ms: 1.06x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 55.4 ms: 1.06x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| raytrace                         | 109 ms                                                         | 117 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.08x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 68.4 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 36.9 ms: 1.10x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.63 ms: 1.11x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.0 ms: 1.12x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.7 ms: 1.12x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.1 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.6 ms: 1.18x slower                                                   |
| many_optionals                   | 200 us                                                         | 236 us: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 260 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 153 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.56x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (1): scimark_sparse_mat_mult
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260824-3.16.0a0-ee521e8/bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.060x faster

# HPT report

- Reliability score: 99.92% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.14x