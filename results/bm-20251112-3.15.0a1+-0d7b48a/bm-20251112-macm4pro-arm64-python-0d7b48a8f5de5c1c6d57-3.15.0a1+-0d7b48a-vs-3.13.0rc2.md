# Results vs. 3.13.0rc2

- fork: python
- ref: 0d7b48a8f5de5c1c6d57
- machine: darwin-arm64
- commit hash: 0d7b48a
- commit date: 2025-11-12
- overall geometric mean: 1.027x faster
- HPT reliability: 93.41%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 228 ms: 2.28x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 230 ms: 2.28x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 231 ms: 1.67x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 142 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.92 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.1 ms: 2.84x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.18x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 47.0 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.68 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 49.1 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a |
|---------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps          | 4.65 ms                                                        | 3.90 ms: 1.19x faster                                                    |
| xml_etree_iterparse | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| tomli_loads         | 1000 ms                                                        | 925 ms: 1.08x faster                                                     |
| xml_etree_parse     | 62.4 ms                                                        | 61.8 ms: 1.01x faster                                                    |
| xml_etree_process   | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                    |
| json_loads          | 10.8 us                                                        | 11.0 us: 1.01x slower                                                    |
| pickle_pure_python  | 130 us                                                         | 146 us: 1.12x slower                                                     |
| Geometric mean      | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (2): xml_etree_generate, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.82 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                    |
| genshi_xml      | 21.4 ms                                                        | 22.2 ms: 1.04x slower                                                    |
| mako            | 4.41 ms                                                        | 4.94 ms: 1.12x slower                                                    |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 228 ms: 2.28x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 230 ms: 2.28x faster                                                     |
| mdp                              | 1.06 sec                                                       | 540 ms: 1.96x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 231 ms: 1.67x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.3 us: 1.34x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| deepcopy                         | 145 us                                                         | 111 us: 1.30x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.3 ms: 1.30x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 142 ms: 1.30x faster                                                     |
| go                               | 72.6 ms                                                        | 56.1 ms: 1.29x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.90 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.68 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| float                            | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.92 ms: 1.08x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 925 ms: 1.08x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 923 us: 1.08x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.92 ms: 1.05x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.2 ms: 1.04x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.7 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.0 ms: 1.03x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 42.6 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.03x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.3 ms: 1.03x faster                                                    |
| sphinx                           | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 122 ms: 1.01x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.8 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.86 ms: 1.00x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 417 us: 1.01x slower                                                     |
| pycparser                        | 470 ms                                                         | 476 ms: 1.01x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.01x slower                                                    |
| fannkuch                         | 179 ms                                                         | 182 ms: 1.02x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.82 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 49.1 ms: 1.02x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 66.5 us: 1.03x slower                                                    |
| thrift                           | 309 us                                                         | 318 us: 1.03x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 41.9 ns: 1.03x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 978 ns: 1.03x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 671 ms: 1.03x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.31 us: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 334 ms: 1.04x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 22.2 ms: 1.04x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.55 us: 1.04x slower                                                    |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.3 ms: 1.05x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.6 ms: 1.06x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.7 ms: 1.07x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 103 ms: 1.08x slower                                                     |
| coverage                         | 31.2 ms                                                        | 33.6 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.8 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.0 ms: 1.10x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.49 us: 1.10x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 176 ms: 1.10x slower                                                     |
| nbody                            | 42.5 ms                                                        | 47.0 ms: 1.11x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.5 ms: 1.11x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 42.1 ms: 1.11x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.94 ms: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.2 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| many_optionals                   | 200 us                                                         | 360 us: 1.80x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.1 ms: 2.84x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.9 ms: 2.85x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (8): dask, async_tree_eager, xml_etree_generate, json, regex_dna, sympy_integrate, scimark_sparse_mat_mult, unpickle_pure_python
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251112-3.15.0a1+-0d7b48a/bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 93.41% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.17x