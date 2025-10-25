# Results vs. 3.13.0rc2

- fork: python
- ref: d78d7a50b06c4ea10d13
- machine: darwin-arm64
- commit hash: d78d7a5
- commit date: 2025-10-24
- overall geometric mean: 1.049x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                    |
| sphinx         | 409 ms                                                         | 395 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 225 ms: 2.34x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 225 ms: 2.31x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 222 ms: 1.83x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 228 ms: 1.70x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.42x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.9 ms: 1.34x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 141 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.8 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 125 ms: 1.22x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.4 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 48.8 ms: 1.15x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.14x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.67 ms: 1.11x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.3 ms: 1.03x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.7 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.6 ms: 1.19x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 886 ms: 1.13x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 34.0 ms: 1.05x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 98.1 us: 1.01x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.75 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.21 ms: 1.04x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.70 ms: 1.03x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.73 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 225 ms: 2.34x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 225 ms: 2.31x faster                                                     |
| mdp                              | 1.06 sec                                                       | 533 ms: 1.98x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 222 ms: 1.83x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 228 ms: 1.70x faster                                                     |
| k_core                           | 1.46 sec                                                       | 905 ms: 1.62x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.43x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.42x faster                                                     |
| deepcopy                         | 145 us                                                         | 103 us: 1.40x faster                                                     |
| go                               | 72.6 ms                                                        | 53.1 ms: 1.37x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 98.9 ms: 1.34x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 141 ms: 1.31x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.9 ms: 1.28x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.6 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.10 us: 1.18x faster                                                    |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| float                            | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.14x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 886 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.67 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| richards                         | 22.1 ms                                                        | 20.3 ms: 1.09x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 919 us: 1.08x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.0 ms: 1.07x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.88 ms: 1.07x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.0 ms: 1.05x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.72 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.7 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                    |
| sphinx                           | 409 ms                                                         | 395 ms: 1.03x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 46.3 ms: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.8 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.70 ms: 1.03x faster                                                    |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 63.3 us: 1.02x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 315 ms: 1.02x faster                                                     |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.39 ms: 1.02x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 39.9 ns: 1.02x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 638 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 98.1 us: 1.01x faster                                                    |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 93.7 ms: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 307 us: 1.01x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.47 us: 1.01x slower                                                    |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| sqlite_synth                     | 948 ns                                                         | 960 ns: 1.01x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.75 ms: 1.01x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.27 us: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.5 ms: 1.02x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.02x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.2 ms: 1.03x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.1 ms: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.21 ms: 1.04x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.9 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.14 ms: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.1 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.88 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                     |
| raytrace                         | 109 ms                                                         | 116 ms: 1.06x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.30 us: 1.07x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.73 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.08x slower                                                     |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 41.3 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.2 ms: 1.11x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 48.2 ms: 1.13x slower                                                    |
| nbody                            | 42.5 ms                                                        | 48.8 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.4 ms: 1.17x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 125 ms: 1.22x slower                                                     |
| many_optionals                   | 200 us                                                         | 362 us: 1.81x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.4 ms: 2.81x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.8 ms: 2.84x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (5): pycparser, dask, bench_thread_pool, deltablue, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251024-3.15.0a1+-d78d7a5/bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1+-d78d7a5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.049x faster

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.16x