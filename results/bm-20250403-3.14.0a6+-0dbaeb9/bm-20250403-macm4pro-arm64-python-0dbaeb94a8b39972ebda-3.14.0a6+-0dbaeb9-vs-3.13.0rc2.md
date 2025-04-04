# Results vs. 3.13.0rc2

- fork: python
- ref: 0dbaeb94a8b39972ebda
- machine: darwin-arm64
- commit hash: 0dbaeb9
- commit date: 2025-04-03
- overall geometric mean: 1.019x faster
- HPT reliability: 55.90%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.00x faster                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 258 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 170 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 43.0 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.4 ms: 3.09x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.6 ms: 1.06x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 48.6 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                    |
| regex_dna      | 94.6 ms                                                        | 99.9 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 926 ms: 1.08x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.2 ms: 1.07x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.2 ms: 1.01x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.7 ms: 1.01x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 103 us: 1.03x slower                                                     |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.04x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 66.5 ms: 1.07x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.01 ms: 1.08x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.92 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.71 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                    |
| mako            | 4.41 ms                                                        | 4.82 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.04x faster                                                     |
| mdp                              | 1.06 sec                                                       | 523 ms: 2.02x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                     |
| k_core                           | 1.46 sec                                                       | 947 ms: 1.55x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.30x faster                                                    |
| deepcopy                         | 145 us                                                         | 112 us: 1.30x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 51.0 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| go                               | 72.6 ms                                                        | 58.0 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 258 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 170 ms: 1.13x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 879 us: 1.13x faster                                                     |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 926 ms: 1.08x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.2 ms: 1.07x faster                                                    |
| float                            | 31.4 ms                                                        | 29.6 ms: 1.06x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                     |
| connected_components             | 208 ms                                                         | 201 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.00 ms: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 935 ns: 1.01x faster                                                     |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| 2to3                             | 112 ms                                                         | 111 ms: 1.00x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 43.0 ms: 1.00x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.1 ms: 1.01x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.59 ms: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.2 ms: 1.01x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 2.88 ms: 1.01x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.10 ms: 1.01x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 65.5 us: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.7 ms: 1.01x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 45.1 ms: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.7 ms: 1.02x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.6 ns: 1.03x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 103 us: 1.03x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.92 ms: 1.03x slower                                                    |
| fannkuch                         | 179 ms                                                         | 185 ms: 1.03x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 49.7 ms: 1.04x slower                                                    |
| richards                         | 22.1 ms                                                        | 22.9 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.04x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.7 ms: 1.04x slower                                                    |
| pycparser                        | 470 ms                                                         | 492 ms: 1.05x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 39.6 ms: 1.05x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 338 ms: 1.05x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 99.9 ms: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 435 us: 1.06x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 686 ms: 1.06x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 66.5 ms: 1.07x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.56 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| json_dumps                       | 4.65 ms                                                        | 5.01 ms: 1.08x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.41 us: 1.08x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.42 ms: 1.08x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.7 ms: 1.08x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.66 us: 1.09x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.82 ms: 1.09x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.9 ms: 1.10x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.0 ms: 1.11x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 48.7 ms: 1.11x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.98 ms: 1.12x slower                                                    |
| raytrace                         | 109 ms                                                         | 122 ms: 1.12x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.6 ms: 1.12x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.71 ms: 1.13x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.69 us: 1.13x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 48.4 ms: 1.13x slower                                                    |
| nbody                            | 42.5 ms                                                        | 48.6 ms: 1.14x slower                                                    |
| many_optionals                   | 200 us                                                         | 231 us: 1.15x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.2 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.64 ms: 1.38x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.4 ms: 3.09x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.019x faster

# HPT report

- Reliability score: 55.90% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.08x