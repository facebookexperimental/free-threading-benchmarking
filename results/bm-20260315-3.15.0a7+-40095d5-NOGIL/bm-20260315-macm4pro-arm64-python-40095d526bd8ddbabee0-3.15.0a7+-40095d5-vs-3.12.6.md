# Results vs. 3.12.6

- fork: python
- ref: 40095d526bd8ddbabee0
- machine: darwin-arm64
- commit hash: 40095d5
- commit date: 2026-03-15
- overall geometric mean: 1.096x faster
- HPT reliability: 99.67%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| docutils       | 1.02 sec                                                 | 994 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.9 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 424 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 237 ms: 2.02x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 246 ms: 2.02x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.85x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.84x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.47x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| async_generators                 | 206 ms                                                   | 190 ms: 1.08x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.6 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.2 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.6 ms: 1.33x faster                                                    |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                     |
| nbody          | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.2 ms: 1.09x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.6 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                    |
| tomli_loads          | 957 ms                                                   | 843 ms: 1.14x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.90 ms: 1.09x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 106 us: 1.03x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.88 ms: 1.23x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.18 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.25x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.7 ms: 1.04x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| mako            | 4.77 ms                                                  | 5.54 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.08 ms: 5.09x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 817 us: 2.46x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 237 ms: 2.02x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 246 ms: 2.02x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.85x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.84x faster                                                     |
| mdp                              | 1.09 sec                                                 | 609 ms: 1.79x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 510 us: 1.63x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| deepcopy                         | 161 us                                                   | 107 us: 1.52x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.47x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.46x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                    |
| float                            | 37.9 ms                                                  | 28.6 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 793 ns: 1.22x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.24 us: 1.19x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.5 ns: 1.17x faster                                                    |
| go                               | 70.0 ms                                                  | 59.8 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                   |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 843 ms: 1.14x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 994 ms: 1.12x faster                                                     |
| pyflate                          | 216 ms                                                   | 194 ms: 1.11x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 55.4 ms: 1.10x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.90 ms: 1.09x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.36 us: 1.09x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 50.2 ms: 1.09x faster                                                    |
| async_generators                 | 206 ms                                                   | 190 ms: 1.08x faster                                                     |
| pycparser                        | 497 ms                                                   | 460 ms: 1.08x faster                                                     |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                     |
| generators                       | 21.9 ms                                                  | 20.5 ms: 1.07x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.7 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.1 ms: 1.07x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.64 us: 1.06x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.2 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.6 ms: 1.04x faster                                                    |
| docutils                         | 1.02 sec                                                 | 994 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                     |
| sphinx                           | 434 ms                                                   | 424 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.9 ms: 1.01x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 672 ms: 1.01x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.6 ms: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.14 ms: 1.02x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.6 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.7 us: 1.02x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.0 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 106 us: 1.03x slower                                                     |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.15 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 26.3 ms: 1.04x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.7 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.20 ms: 1.05x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 54.3 ms: 1.06x slower                                                    |
| thrift                           | 322 us                                                   | 341 us: 1.06x slower                                                     |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 61.5 ms: 1.07x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 44.3 ms: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 192 ms: 1.15x slower                                                     |
| shortest_path                    | 219 ms                                                   | 252 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.54 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 56.1 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 47.1 ms: 1.18x slower                                                    |
| connected_components             | 201 ms                                                   | 244 ms: 1.22x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.88 ms: 1.23x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.18 ms: 1.26x slower                                                    |
| many_optionals                   | 195 us                                                   | 269 us: 1.38x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 583 us: 1.39x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.5 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.2 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (4): fannkuch, xml_etree_process, dask, pprint_safe_repr
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260315-3.15.0a7+-40095d5-NOGIL/bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7+-40095d5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.096x faster

# HPT report

- Reliability score: 99.67% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.37x