# Results vs. 3.12.6

- fork: python
- ref: 0dbaeb94a8b39972ebda
- machine: darwin-arm64
- commit hash: 0dbaeb9
- commit date: 2025-04-03
- overall geometric mean: 1.099x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| sphinx         | 434 ms                                                   | 411 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 2.00x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 257 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 258 ms: 1.29x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_generators                 | 206 ms                                                   | 170 ms: 1.21x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 43.0 ms: 1.06x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.4 ms: 2.78x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.6 ms: 1.28x faster                                                    |
| nbody          | 54.2 ms                                                  | 48.6 ms: 1.12x faster                                                    |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 99.9 ms: 1.00x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 10.2 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.2 ms: 1.19x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.2 ms: 1.07x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                    |
| tomli_loads          | 957 ms                                                   | 926 ms: 1.03x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 66.5 ms: 1.02x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 103 us: 1.00x faster                                                     |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 5.01 ms: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.92 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.71 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.7 ms: 1.00x faster                                                    |
| mako            | 4.77 ms                                                  | 4.82 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.64 ms: 2.40x faster                                                    |
| mdp                              | 1.09 sec                                                 | 523 ms: 2.09x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 2.00x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.45x faster                                                    |
| deepcopy                         | 161 us                                                   | 112 us: 1.45x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 257 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 258 ms: 1.29x faster                                                     |
| float                            | 37.9 ms                                                  | 29.6 ms: 1.28x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.69 us: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.6 ns: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 170 ms: 1.21x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.2 ms: 1.21x faster                                                    |
| go                               | 70.0 ms                                                  | 58.0 ms: 1.21x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.8 ms: 1.20x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 51.0 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.2 ms: 1.19x faster                                                    |
| raytrace                         | 145 ms                                                   | 122 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| k_core                           | 1.12 sec                                                 | 947 ms: 1.18x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.16x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                    |
| nbody                            | 54.2 ms                                                  | 48.6 ms: 1.12x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 48.7 ms: 1.12x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.56 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 65.5 us: 1.08x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 36.2 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.0 ms: 1.07x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.1 ms: 1.07x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.41 us: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 40.9 ms: 1.06x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 48.4 ms: 1.06x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.0 ms: 1.06x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.59 ms: 1.06x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.88 ms: 1.06x faster                                                    |
| sphinx                           | 434 ms                                                   | 411 ms: 1.05x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.66 us: 1.05x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.98 ms: 1.05x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 45.1 ms: 1.04x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 935 ns: 1.03x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 926 ms: 1.03x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.6 ms: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                     |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 66.5 ms: 1.02x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.7 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.01x faster                                                     |
| pycparser                        | 497 ms                                                   | 492 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.7 ms: 1.00x faster                                                    |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 103 us: 1.00x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 99.9 ms: 1.00x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.82 ms: 1.01x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 25.7 ms: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                     |
| richards                         | 22.4 ms                                                  | 22.9 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 338 ms: 1.03x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 686 ms: 1.03x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 435 us: 1.04x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.7 ms: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.42 ms: 1.05x slower                                                    |
| fannkuch                         | 176 ms                                                   | 185 ms: 1.05x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 879 us: 1.06x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 10.2 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.92 ms: 1.11x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.71 ms: 1.18x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.01 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.7 ms: 1.18x slower                                                    |
| many_optionals                   | 195 us                                                   | 231 us: 1.18x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.10 ms: 1.19x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.4 ms: 2.78x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (4): json, gc_traversal, bench_mp_pool, connected_components
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.099x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.13x