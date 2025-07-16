# Results vs. 3.12.6

- fork: python
- ref: cb59eaefeda5ff44ac0c
- machine: darwin-arm64
- commit hash: cb59eae
- commit date: 2025-07-15
- overall geometric mean: 1.100x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                   |
| sphinx         | 434 ms                                                   | 409 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 257 ms: 1.86x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.25x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.9 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.8 ms: 2.76x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.9 ms: 1.23x faster                                                   |
| nbody          | 54.2 ms                                                  | 49.5 ms: 1.10x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.7 ms: 1.12x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.6 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.84 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.7 ms: 1.18x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.6 ms: 1.05x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 99.5 us: 1.03x faster                                                   |
| tomli_loads          | 957 ms                                                   | 930 ms: 1.03x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.44 ms: 1.04x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 149 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.56 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.12 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.1 ms: 1.01x slower                                                   |
| mako            | 4.77 ms                                                  | 4.85 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.86 ms: 2.11x faster                                                   |
| mdp                              | 1.09 sec                                                 | 518 ms: 2.11x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 257 ms: 1.86x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.45x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.45x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.42 us: 1.33x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.25x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.0 ns: 1.24x faster                                                   |
| go                               | 70.0 ms                                                  | 56.4 ms: 1.24x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                   |
| float                            | 37.9 ms                                                  | 30.9 ms: 1.23x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 45.2 ms: 1.20x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 51.1 ms: 1.19x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.5 ms: 1.19x faster                                                   |
| raytrace                         | 145 ms                                                   | 122 ms: 1.19x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.7 ms: 1.18x faster                                                   |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| k_core                           | 1.12 sec                                                 | 948 ms: 1.18x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.7 ms: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 39.0 ms: 1.11x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 63.8 us: 1.11x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.56 ms: 1.10x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                    |
| nbody                            | 54.2 ms                                                  | 49.5 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.90 ms: 1.09x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.7 ms: 1.08x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.82 ms: 1.08x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.9 ms: 1.08x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.47 ms: 1.07x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.40 us: 1.07x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.9 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 409 ms: 1.06x faster                                                    |
| thrift                           | 322 us                                                   | 304 us: 1.06x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.6 ms: 1.05x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.5 ms: 1.04x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.4 ms: 1.04x faster                                                   |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 99.5 us: 1.03x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 930 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.9 ms: 1.03x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 97.6 ms: 1.02x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.4 ms: 1.02x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 50.5 ms: 1.02x faster                                                   |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| meteor_contest                   | 47.7 ms                                                  | 47.9 ms: 1.00x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.00x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                    |
| shortest_path                    | 219 ms                                                   | 220 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.1 ms: 1.01x slower                                                   |
| 2to3                             | 114 ms                                                   | 116 ms: 1.01x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.85 ms: 1.02x slower                                                   |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 677 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 335 ms: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 205 ms: 1.02x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.84 ms: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.03x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.44 ms: 1.04x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 440 us: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 149 us: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.56 ms: 1.07x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.12 ms: 1.07x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.1 ms: 1.11x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 939 us: 1.13x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.04 ms: 1.16x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.3 ms: 1.24x slower                                                   |
| many_optionals                   | 195 us                                                   | 251 us: 1.29x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.8 ms: 2.76x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (3): json_loads, pycparser, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x