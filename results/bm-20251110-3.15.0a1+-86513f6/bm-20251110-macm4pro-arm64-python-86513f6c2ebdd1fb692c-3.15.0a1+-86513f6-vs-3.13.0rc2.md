# Results vs. 3.13.0rc2

- fork: python
- ref: 86513f6c2ebdd1fb692c
- machine: darwin-arm64
- commit hash: 86513f6
- commit date: 2025-11-10
- overall geometric mean: 1.026x faster
- HPT reliability: 87.39%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| html5lib       | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 403 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 227 ms: 2.29x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 229 ms: 2.29x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 228 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 230 ms: 1.68x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 142 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.96 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 42.9 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.7 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.18x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 49.5 ms: 1.17x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                    |
| regex_dna      | 94.6 ms                                                        | 96.1 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.90 ms: 1.19x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.1 ms: 1.15x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 901 ms: 1.11x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 62.1 ms: 1.00x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 100 us: 1.01x slower                                                     |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.02x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.27 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                    |
| genshi_xml      | 21.4 ms                                                        | 22.1 ms: 1.03x slower                                                    |
| mako            | 4.41 ms                                                        | 4.78 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 227 ms: 2.29x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 229 ms: 2.29x faster                                                     |
| mdp                              | 1.06 sec                                                       | 539 ms: 1.96x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 228 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 230 ms: 1.68x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.1 us: 1.36x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                     |
| go                               | 72.6 ms                                                        | 55.5 ms: 1.31x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 142 ms: 1.30x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.8 ms: 1.29x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.90 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                                     |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.1 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 901 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| float                            | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.96 ms: 1.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 927 us: 1.07x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.87 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.2 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.0 ms: 1.03x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 24.0 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.5 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                    |
| sphinx                           | 409 ms                                                         | 403 ms: 1.01x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.9 ms: 1.01x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.83 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 62.1 ms: 1.00x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.56 ms: 1.00x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 100 us: 1.01x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 65.2 us: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                    |
| pycparser                        | 470 ms                                                         | 476 ms: 1.01x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.80 ms: 1.01x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 418 us: 1.01x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.1 ms: 1.02x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.3 ns: 1.02x slower                                                    |
| thrift                           | 309 us                                                         | 316 us: 1.02x slower                                                     |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| fannkuch                         | 179 ms                                                         | 183 ms: 1.02x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 666 ms: 1.02x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 331 ms: 1.03x slower                                                     |
| sqlite_synth                     | 948 ns                                                         | 979 ns: 1.03x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.31 us: 1.03x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.53 us: 1.03x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.1 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.6 ms: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.27 ms: 1.05x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 39.6 ms: 1.06x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.7 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.78 ms: 1.08x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.3 ms: 1.09x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.40 us: 1.09x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 104 ms: 1.09x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 57.2 ms: 1.09x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 176 ms: 1.11x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.2 ms: 1.11x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.12x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 42.5 ms: 1.12x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 48.8 ms: 1.14x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.3 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.17x slower                                                     |
| nbody                            | 42.5 ms                                                        | 49.5 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                    |
| many_optionals                   | 200 us                                                         | 361 us: 1.80x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.7 ms: 2.86x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.9 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (3): docutils, dask, spectral_norm
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251110-3.15.0a1+-86513f6/bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.026x faster

# HPT report

- Reliability score: 87.39% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.17x