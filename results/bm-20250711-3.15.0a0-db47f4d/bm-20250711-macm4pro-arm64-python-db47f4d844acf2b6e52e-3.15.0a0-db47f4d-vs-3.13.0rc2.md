# Results vs. 3.13.0rc2

- fork: python
- ref: db47f4d844acf2b6e52e
- machine: darwin-arm64
- commit hash: db47f4d
- commit date: 2025-07-11
- overall geometric mean: 1.010x faster
- HPT reliability: 65.98%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.07 sec: 1.03x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.6 ms: 1.06x slower                                                   |
| sphinx         | 409 ms                                                         | 418 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 254 ms: 2.07x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 257 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 257 ms: 1.57x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.24x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 113 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 268 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.8 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 133 ms: 1.29x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.8 ms: 3.10x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 31.0 ms: 1.01x faster                                                   |
| pidigits       | 166 ms                                                         | 170 ms: 1.02x slower                                                    |
| nbody          | 42.5 ms                                                        | 49.3 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 99.2 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 945 ms: 1.06x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.3 ms: 1.04x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.54 ms: 1.03x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.9 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.0 ms: 1.01x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.6 ms: 1.01x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.01x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.02x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.79 ms: 1.02x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 22.2 ms: 1.04x slower                                                   |
| mako            | 4.41 ms                                                        | 4.97 ms: 1.13x slower                                                   |
| django_template | 12.5 ms                                                        | 15.8 ms: 1.27x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 254 ms: 2.07x faster                                                    |
| mdp                              | 1.06 sec                                                       | 523 ms: 2.02x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 257 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 257 ms: 1.57x faster                                                    |
| k_core                           | 1.46 sec                                                       | 955 ms: 1.53x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| deepcopy                         | 145 us                                                         | 112 us: 1.29x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.29x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 50.8 ms: 1.26x faster                                                   |
| go                               | 72.6 ms                                                        | 58.1 ms: 1.25x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.24x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 113 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 268 ms: 1.13x faster                                                    |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.19 us: 1.09x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 945 ms: 1.06x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.3 ms: 1.04x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 965 us: 1.03x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.54 ms: 1.03x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 60.9 ms: 1.02x faster                                                   |
| connected_components             | 208 ms                                                         | 204 ms: 1.02x faster                                                    |
| float                            | 31.4 ms                                                        | 31.0 ms: 1.01x faster                                                   |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.03 ms: 1.01x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 64.0 us: 1.01x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.8 ms: 1.01x faster                                                   |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 307 us: 1.01x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.7 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.0 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.60 ms: 1.01x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.6 ms: 1.01x slower                                                   |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.1 ns: 1.01x slower                                                   |
| pathlib                          | 11.1 ms                                                        | 11.3 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.01x slower                                                   |
| richards                         | 22.1 ms                                                        | 22.4 ms: 1.01x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.79 ms: 1.02x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.02x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                   |
| sphinx                           | 409 ms                                                         | 418 ms: 1.02x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.2 ms: 1.02x slower                                                   |
| pidigits                         | 166 ms                                                         | 170 ms: 1.02x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 971 ns: 1.03x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.07 sec: 1.03x slower                                                  |
| meteor_contest                   | 47.9 ms                                                        | 49.1 ms: 1.03x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.11 ms: 1.03x slower                                                   |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.2 ms: 1.04x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 45.6 ms: 1.04x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 336 ms: 1.04x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 679 ms: 1.05x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 99.2 ms: 1.05x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.6 ms: 1.06x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 438 us: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.8 ms: 1.07x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.91 ms: 1.07x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.56 ms: 1.08x slower                                                   |
| pycparser                        | 470 ms                                                         | 509 ms: 1.08x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.8 ms: 1.08x slower                                                   |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.6 ms: 1.10x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.68 us: 1.10x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 57.5 ms: 1.10x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.46 us: 1.10x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.51 us: 1.10x slower                                                   |
| raytrace                         | 109 ms                                                         | 122 ms: 1.12x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.97 ms: 1.13x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.4 ms: 1.14x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                                    |
| nbody                            | 42.5 ms                                                        | 49.3 ms: 1.16x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 50.3 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.6 ms: 1.18x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 251 us: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.8 ms: 1.27x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 133 ms: 1.29x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.88 ms: 1.58x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.8 ms: 3.10x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (1): hexiom
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.010x faster

# HPT report

- Reliability score: 65.98% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.10x