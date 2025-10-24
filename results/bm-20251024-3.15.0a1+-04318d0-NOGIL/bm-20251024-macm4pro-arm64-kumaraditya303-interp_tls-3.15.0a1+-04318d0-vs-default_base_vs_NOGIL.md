# Results vs. default_base_vs_NOGIL

- fork: kumaraditya303
- ref: interp_tls
- machine: darwin-arm64
- commit hash: 04318d0
- commit date: 2025-10-24
- overall geometric mean: 1.011x slower
- HPT reliability: 96.81%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 118 ms                                                                   | 125 ms: 1.06x slower                                                   |
| docutils       | 1.06 sec                                                                 | 1.01 sec: 1.05x faster                                                 |
| sphinx         | 409 ms                                                                   | 418 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 232 ms                                                                   | 198 ms: 1.17x faster                                                   |
| async_tree_none_tg               | 103 ms                                                                   | 88.3 ms: 1.16x faster                                                  |
| async_tree_io_tg                 | 230 ms                                                                   | 201 ms: 1.14x faster                                                   |
| async_tree_memoization_tg        | 142 ms                                                                   | 125 ms: 1.13x faster                                                   |
| async_tree_eager_memoization_tg  | 128 ms                                                                   | 113 ms: 1.13x faster                                                   |
| async_tree_eager_io              | 232 ms                                                                   | 209 ms: 1.11x faster                                                   |
| async_tree_memoization           | 144 ms                                                                   | 132 ms: 1.10x faster                                                   |
| async_tree_io                    | 233 ms                                                                   | 213 ms: 1.09x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 258 ms                                                                   | 237 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 246 ms                                                                   | 229 ms: 1.07x faster                                                   |
| async_tree_eager_tg              | 84.7 ms                                                                  | 79.5 ms: 1.07x faster                                                  |
| async_tree_cpu_io_mixed          | 258 ms                                                                   | 245 ms: 1.05x faster                                                   |
| async_tree_none                  | 104 ms                                                                   | 102 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 226 ms                                                                   | 225 ms: 1.01x faster                                                   |
| async_tree_eager_memoization     | 109 ms                                                                   | 111 ms: 1.01x slower                                                   |
| coroutines                       | 10.3 ms                                                                  | 10.6 ms: 1.02x slower                                                  |
| async_generators                 | 180 ms                                                                   | 184 ms: 1.02x slower                                                   |
| async_tree_eager                 | 44.3 ms                                                                  | 49.7 ms: 1.12x slower                                                  |
| Geometric mean                   | (ref)                                                                    | 1.06x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 168 ms                                                                   | 165 ms: 1.02x faster                                                   |
| float          | 30.7 ms                                                                  | 30.1 ms: 1.02x faster                                                  |
| nbody          | 52.2 ms                                                                  | 61.0 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                                    | 1.04x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 9.84 ms                                                                  | 9.29 ms: 1.06x faster                                                  |
| regex_dna      | 95.4 ms                                                                  | 94.6 ms: 1.01x faster                                                  |
| regex_effbot   | 1.44 ms                                                                  | 1.43 ms: 1.01x faster                                                  |
| regex_compile  | 50.7 ms                                                                  | 53.9 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 63.9 ms                                                                  | 58.7 ms: 1.09x faster                                                  |
| xml_etree_iterparse  | 40.3 ms                                                                  | 38.4 ms: 1.05x faster                                                  |
| json_dumps           | 4.03 ms                                                                  | 4.07 ms: 1.01x slower                                                  |
| tomli_loads          | 967 ms                                                                   | 977 ms: 1.01x slower                                                   |
| pickle_pure_python   | 152 us                                                                   | 154 us: 1.01x slower                                                   |
| json_loads           | 11.0 us                                                                  | 11.5 us: 1.05x slower                                                  |
| xml_etree_generate   | 35.7 ms                                                                  | 37.4 ms: 1.05x slower                                                  |
| xml_etree_process    | 25.7 ms                                                                  | 27.3 ms: 1.06x slower                                                  |
| unpickle_pure_python | 103 us                                                                   | 112 us: 1.09x slower                                                   |
| Geometric mean       | (ref)                                                                    | 1.02x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 8.90 ms                                                                  | 9.74 ms: 1.09x slower                                                  |
| python_startup_no_site | 6.35 ms                                                                  | 7.08 ms: 1.12x slower                                                  |
| Geometric mean         | (ref)                                                                    | 1.10x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 16.1 ms                                                                  | 16.7 ms: 1.04x slower                                                  |
| genshi_xml      | 23.1 ms                                                                  | 25.2 ms: 1.09x slower                                                  |
| genshi_text     | 10.5 ms                                                                  | 12.0 ms: 1.15x slower                                                  |
| mako            | 4.94 ms                                                                  | 5.81 ms: 1.18x slower                                                  |
| Geometric mean  | (ref)                                                                    | 1.11x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal                     | 2.10 ms                                                                  | 763 us: 2.75x faster                                                   |
| create_gc_cycles                 | 943 us                                                                   | 474 us: 1.99x faster                                                   |
| sqlite_synth                     | 977 ns                                                                   | 825 ns: 1.18x faster                                                   |
| async_tree_eager_io_tg           | 232 ms                                                                   | 198 ms: 1.17x faster                                                   |
| async_tree_none_tg               | 103 ms                                                                   | 88.3 ms: 1.16x faster                                                  |
| async_tree_io_tg                 | 230 ms                                                                   | 201 ms: 1.14x faster                                                   |
| async_tree_memoization_tg        | 142 ms                                                                   | 125 ms: 1.13x faster                                                   |
| async_tree_eager_memoization_tg  | 128 ms                                                                   | 113 ms: 1.13x faster                                                   |
| async_tree_eager_io              | 232 ms                                                                   | 209 ms: 1.11x faster                                                   |
| async_tree_memoization           | 144 ms                                                                   | 132 ms: 1.10x faster                                                   |
| async_tree_io                    | 233 ms                                                                   | 213 ms: 1.09x faster                                                   |
| xml_etree_parse                  | 63.9 ms                                                                  | 58.7 ms: 1.09x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 258 ms                                                                   | 237 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 246 ms                                                                   | 229 ms: 1.07x faster                                                   |
| async_tree_eager_tg              | 84.7 ms                                                                  | 79.5 ms: 1.07x faster                                                  |
| regex_v8                         | 9.84 ms                                                                  | 9.29 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed          | 258 ms                                                                   | 245 ms: 1.05x faster                                                   |
| docutils                         | 1.06 sec                                                                 | 1.01 sec: 1.05x faster                                                 |
| fannkuch                         | 196 ms                                                                   | 187 ms: 1.05x faster                                                   |
| xml_etree_iterparse              | 40.3 ms                                                                  | 38.4 ms: 1.05x faster                                                  |
| pycparser                        | 490 ms                                                                   | 477 ms: 1.03x faster                                                   |
| dulwich_log                      | 19.8 ms                                                                  | 19.3 ms: 1.03x faster                                                  |
| bpe_tokeniser                    | 2.08 sec                                                                 | 2.03 sec: 1.03x faster                                                 |
| pidigits                         | 168 ms                                                                   | 165 ms: 1.02x faster                                                   |
| float                            | 30.7 ms                                                                  | 30.1 ms: 1.02x faster                                                  |
| async_tree_none                  | 104 ms                                                                   | 102 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                                  | 10.9 ms: 1.02x faster                                                  |
| regex_dna                        | 95.4 ms                                                                  | 94.6 ms: 1.01x faster                                                  |
| regex_effbot                     | 1.44 ms                                                                  | 1.43 ms: 1.01x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 226 ms                                                                   | 225 ms: 1.01x faster                                                   |
| json_dumps                       | 4.03 ms                                                                  | 4.07 ms: 1.01x slower                                                  |
| tomli_loads                      | 967 ms                                                                   | 977 ms: 1.01x slower                                                   |
| json                             | 1.98 ms                                                                  | 2.00 ms: 1.01x slower                                                  |
| async_tree_eager_memoization     | 109 ms                                                                   | 111 ms: 1.01x slower                                                   |
| pickle_pure_python               | 152 us                                                                   | 154 us: 1.01x slower                                                   |
| dask                             | 523 ms                                                                   | 530 ms: 1.01x slower                                                   |
| bench_mp_pool                    | 42.1 ms                                                                  | 42.7 ms: 1.02x slower                                                  |
| scimark_fft                      | 132 ms                                                                   | 135 ms: 1.02x slower                                                   |
| coroutines                       | 10.3 ms                                                                  | 10.6 ms: 1.02x slower                                                  |
| sphinx                           | 409 ms                                                                   | 418 ms: 1.02x slower                                                   |
| telco                            | 3.01 ms                                                                  | 3.08 ms: 1.02x slower                                                  |
| async_generators                 | 180 ms                                                                   | 184 ms: 1.02x slower                                                   |
| sqlglot_v2_normalize             | 48.9 ms                                                                  | 50.2 ms: 1.03x slower                                                  |
| sqlglot_v2_optimize              | 23.9 ms                                                                  | 24.7 ms: 1.04x slower                                                  |
| generators                       | 18.7 ms                                                                  | 19.4 ms: 1.04x slower                                                  |
| many_optionals                   | 378 us                                                                   | 393 us: 1.04x slower                                                   |
| subparsers                       | 18.6 ms                                                                  | 19.3 ms: 1.04x slower                                                  |
| django_template                  | 16.1 ms                                                                  | 16.7 ms: 1.04x slower                                                  |
| sqlglot_v2_transpile             | 699 us                                                                   | 729 us: 1.04x slower                                                   |
| json_loads                       | 11.0 us                                                                  | 11.5 us: 1.05x slower                                                  |
| xml_etree_generate               | 35.7 ms                                                                  | 37.4 ms: 1.05x slower                                                  |
| logging_simple                   | 2.43 us                                                                  | 2.55 us: 1.05x slower                                                  |
| pprint_safe_repr                 | 338 ms                                                                   | 356 ms: 1.05x slower                                                   |
| shortest_path                    | 223 ms                                                                   | 235 ms: 1.05x slower                                                   |
| deepcopy                         | 114 us                                                                   | 120 us: 1.05x slower                                                   |
| sqlglot_v2_parse                 | 573 us                                                                   | 607 us: 1.06x slower                                                   |
| sympy_integrate                  | 7.64 ms                                                                  | 8.09 ms: 1.06x slower                                                  |
| sympy_sum                        | 57.9 ms                                                                  | 61.3 ms: 1.06x slower                                                  |
| 2to3                             | 118 ms                                                                   | 125 ms: 1.06x slower                                                   |
| pprint_pformat                   | 684 ms                                                                   | 725 ms: 1.06x slower                                                   |
| xml_etree_process                | 25.7 ms                                                                  | 27.3 ms: 1.06x slower                                                  |
| regex_compile                    | 50.7 ms                                                                  | 53.9 ms: 1.06x slower                                                  |
| logging_silent                   | 43.1 ns                                                                  | 46.0 ns: 1.07x slower                                                  |
| logging_format                   | 2.65 us                                                                  | 2.83 us: 1.07x slower                                                  |
| thrift                           | 322 us                                                                   | 344 us: 1.07x slower                                                   |
| scimark_sor                      | 52.8 ms                                                                  | 56.6 ms: 1.07x slower                                                  |
| connected_components             | 207 ms                                                                   | 223 ms: 1.07x slower                                                   |
| go                               | 58.8 ms                                                                  | 63.2 ms: 1.07x slower                                                  |
| sympy_str                        | 105 ms                                                                   | 113 ms: 1.08x slower                                                   |
| deepcopy_memo                    | 12.5 us                                                                  | 13.6 us: 1.08x slower                                                  |
| sympy_expand                     | 178 ms                                                                   | 193 ms: 1.08x slower                                                   |
| deepcopy_reduce                  | 1.19 us                                                                  | 1.29 us: 1.09x slower                                                  |
| chaos                            | 27.5 ms                                                                  | 29.9 ms: 1.09x slower                                                  |
| nqueens                          | 41.0 ms                                                                  | 44.6 ms: 1.09x slower                                                  |
| genshi_xml                       | 23.1 ms                                                                  | 25.2 ms: 1.09x slower                                                  |
| unpickle_pure_python             | 103 us                                                                   | 112 us: 1.09x slower                                                   |
| k_core                           | 913 ms                                                                   | 996 ms: 1.09x slower                                                   |
| deltablue                        | 1.52 ms                                                                  | 1.66 ms: 1.09x slower                                                  |
| richards_super                   | 25.2 ms                                                                  | 27.5 ms: 1.09x slower                                                  |
| python_startup                   | 8.90 ms                                                                  | 9.74 ms: 1.09x slower                                                  |
| richards                         | 22.1 ms                                                                  | 24.2 ms: 1.10x slower                                                  |
| comprehensions                   | 7.77 us                                                                  | 8.51 us: 1.10x slower                                                  |
| raytrace                         | 122 ms                                                                   | 134 ms: 1.10x slower                                                   |
| hexiom                           | 2.95 ms                                                                  | 3.25 ms: 1.10x slower                                                  |
| scimark_monte_carlo              | 31.0 ms                                                                  | 34.2 ms: 1.10x slower                                                  |
| meteor_contest                   | 51.3 ms                                                                  | 56.9 ms: 1.11x slower                                                  |
| python_startup_no_site           | 6.35 ms                                                                  | 7.08 ms: 1.12x slower                                                  |
| crypto_pyaes                     | 38.5 ms                                                                  | 43.0 ms: 1.12x slower                                                  |
| mdp                              | 553 ms                                                                   | 619 ms: 1.12x slower                                                   |
| async_tree_eager                 | 44.3 ms                                                                  | 49.7 ms: 1.12x slower                                                  |
| scimark_lu                       | 50.7 ms                                                                  | 56.9 ms: 1.12x slower                                                  |
| typing_runtime_protocols         | 66.8 us                                                                  | 75.1 us: 1.13x slower                                                  |
| genshi_text                      | 10.5 ms                                                                  | 12.0 ms: 1.15x slower                                                  |
| spectral_norm                    | 44.6 ms                                                                  | 51.1 ms: 1.15x slower                                                  |
| nbody                            | 52.2 ms                                                                  | 61.0 ms: 1.17x slower                                                  |
| mako                             | 4.94 ms                                                                  | 5.81 ms: 1.18x slower                                                  |
| scimark_sparse_mat_mult          | 1.91 ms                                                                  | 2.25 ms: 1.18x slower                                                  |
| coverage                         | 32.2 ms                                                                  | 40.9 ms: 1.27x slower                                                  |
| bench_thread_pool                | 420 us                                                                   | 548 us: 1.30x slower                                                   |
| Geometric mean                   | (ref)                                                                    | 1.01x slower                                                           |

Benchmark hidden because not significant (4): pylint, asyncio_websockets, pyflate, html5lib

- Geometric mean (including insignificant results): 1.011x slower

# HPT report

- Reliability score: 96.81% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.13x