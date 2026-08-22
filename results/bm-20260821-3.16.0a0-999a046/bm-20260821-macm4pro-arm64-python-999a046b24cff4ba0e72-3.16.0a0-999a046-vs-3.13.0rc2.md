# Results vs. 3.13.0rc2

- fork: python
- ref: 999a046b24cff4ba0e72
- machine: darwin-arm64
- commit hash: 999a046
- commit date: 2026-08-21
- overall geometric mean: 1.041x faster
- HPT reliability: 97.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 962 ms: 1.09x faster                                                    |
| html5lib       | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 316 ms: 1.66x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 341 ms: 1.53x faster                                                    |
| async_generators                 | 193 ms                                                         | 145 ms: 1.33x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 319 ms: 1.21x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 335 ms: 1.21x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 124 ms: 1.15x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.90 ms: 1.09x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 176 ms: 1.06x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 118 ms: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 297 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 230 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 268 ms: 1.29x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 105 ms: 3.64x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (3): async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| nbody          | 42.5 ms                                                        | 41.8 ms: 1.02x faster                                                   |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.20 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.6 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 55.5 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.63 ms: 1.28x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 867 ms: 1.15x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.2 us: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.3 ms: 1.04x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 142 us: 1.09x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 69.7 ms: 1.12x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.09 ms: 1.05x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.30 ms: 1.06x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.68 ms: 1.06x slower                                                   |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 528 ms: 2.00x faster                                                    |
| pylint                           | 106 ms                                                         | 57.3 ms: 1.84x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 316 ms: 1.66x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 341 ms: 1.53x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.16 ms: 1.51x faster                                                   |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.47x faster                                                    |
| deepcopy                         | 145 us                                                         | 101 us: 1.44x faster                                                    |
| go                               | 72.6 ms                                                        | 53.5 ms: 1.35x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 12.3 us: 1.34x faster                                                   |
| async_generators                 | 193 ms                                                         | 145 ms: 1.33x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.5 ms: 1.29x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 50.0 us: 1.29x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.63 ms: 1.28x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 319 ms: 1.21x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 335 ms: 1.21x faster                                                    |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 841 us: 1.18x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.10 us: 1.18x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.20 ms: 1.16x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 867 ms: 1.15x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 124 ms: 1.15x faster                                                    |
| fannkuch                         | 179 ms                                                         | 164 ms: 1.09x faster                                                    |
| docutils                         | 1.05 sec                                                       | 962 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.90 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.08x faster                                                  |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.6 ms: 1.07x faster                                                   |
| float                            | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.87 ms: 1.07x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.1 ms: 1.06x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.06x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 176 ms: 1.06x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.5 ms: 1.05x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.95 ms: 1.05x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.72 ms: 1.05x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 35.7 ms: 1.04x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 42.2 ms: 1.04x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 118 ms: 1.03x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 92.6 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 316 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                   |
| nbody                            | 42.5 ms                                                        | 41.8 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 297 ms: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 934 ns: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.2 us: 1.01x faster                                                   |
| connected_components             | 208 ms                                                         | 207 ms: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 652 ms: 1.00x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.56 ms: 1.00x slower                                                   |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.46 us: 1.01x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 6.85 us: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 230 ms: 1.02x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 423 us: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.84 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.6 ms: 1.04x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.3 ms: 1.04x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.2 ns: 1.04x slower                                                   |
| thrift                           | 309 us                                                         | 321 us: 1.04x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.04x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.09 ms: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.05x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.6 ms: 1.05x slower                                                   |
| pycparser                        | 470 ms                                                         | 496 ms: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.30 ms: 1.06x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.68 ms: 1.06x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.1 ms: 1.07x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 172 ms: 1.08x slower                                                    |
| 2to3                             | 112 ms                                                         | 121 ms: 1.09x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 142 us: 1.09x slower                                                    |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 69.7 ms: 1.12x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.0 ms: 1.13x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.9 ms: 1.14x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 55.5 ms: 1.16x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 50.4 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.5 ms: 1.20x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                   |
| many_optionals                   | 200 us                                                         | 246 us: 1.23x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 268 ms: 1.29x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 105 ms: 3.64x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (6): async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed, sphinx, json_loads, logging_simple
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260821-3.16.0a0-999a046/bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.041x faster

# HPT report

- Reliability score: 97.98% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.15x