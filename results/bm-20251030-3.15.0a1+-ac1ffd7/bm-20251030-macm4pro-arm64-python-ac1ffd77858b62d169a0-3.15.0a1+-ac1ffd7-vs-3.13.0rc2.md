# Results vs. 3.13.0rc2

- fork: python
- ref: ac1ffd77858b62d169a0
- machine: darwin-arm64
- commit hash: ac1ffd7
- commit date: 2025-10-30
- overall geometric mean: 1.027x faster
- HPT reliability: 88.69%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 404 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 225 ms: 2.31x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 230 ms: 2.28x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 230 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 233 ms: 1.66x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 141 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.30x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.6 ms: 2.89x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.17x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 49.9 ms: 1.17x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 94.2 ms: 1.00x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.97 ms: 1.17x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.3 ms: 1.14x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 893 ms: 1.12x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 62.0 ms: 1.01x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.0 ms: 1.01x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.6 ms: 1.01x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 102 us: 1.02x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.75 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.19 ms: 1.04x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.0 ms: 1.01x slower                                                    |
| genshi_xml      | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                    |
| mako            | 4.41 ms                                                        | 4.88 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 225 ms: 2.31x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 230 ms: 2.28x faster                                                     |
| mdp                              | 1.06 sec                                                       | 542 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 230 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 233 ms: 1.66x faster                                                     |
| k_core                           | 1.46 sec                                                       | 900 ms: 1.63x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.1 us: 1.36x faster                                                    |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 141 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.30x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.4 ms: 1.30x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                     |
| go                               | 72.6 ms                                                        | 57.1 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.97 ms: 1.17x faster                                                    |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.3 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 893 ms: 1.12x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 915 us: 1.09x faster                                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.88 ms: 1.07x faster                                                    |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.02 sec: 1.06x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.03x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.1 ms: 1.03x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.3 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 42.8 ms: 1.02x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.74 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 404 ms: 1.01x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 62.0 ms: 1.01x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 94.2 ms: 1.00x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 123 ms: 1.00x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 36.0 ms: 1.01x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.0 ms: 1.01x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.6 ms: 1.01x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 417 us: 1.01x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.75 ms: 1.01x slower                                                    |
| thrift                           | 309 us                                                         | 314 us: 1.02x slower                                                     |
| richards                         | 22.1 ms                                                        | 22.5 ms: 1.02x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 102 us: 1.02x slower                                                     |
| pycparser                        | 470 ms                                                         | 482 ms: 1.02x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 669 ms: 1.03x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                    |
| fannkuch                         | 179 ms                                                         | 184 ms: 1.03x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.03x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.5 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 66.9 us: 1.04x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 333 ms: 1.04x slower                                                     |
| sqlite_synth                     | 948 ns                                                         | 982 ns: 1.04x slower                                                     |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.19 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.8 ms: 1.04x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.33 us: 1.04x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.56 us: 1.05x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.9 ns: 1.06x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                     |
| coverage                         | 31.2 ms                                                        | 33.3 ms: 1.07x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.9 ms: 1.07x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 103 ms: 1.07x slower                                                     |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.08x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 40.9 ms: 1.08x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.7 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.88 ms: 1.11x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.5 ms: 1.11x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                     |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.12x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.61 us: 1.12x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.7 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| nbody                            | 42.5 ms                                                        | 49.9 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 369 us: 1.84x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.6 ms: 2.89x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.2 ms: 2.91x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (7): json, dask, json_loads, sympy_integrate, docutils, hexiom, async_tree_eager
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251030-3.15.0a1+-ac1ffd7/bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 88.69% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.15x