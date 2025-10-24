# Results vs. base

- fork: kumaraditya303
- ref: interp_tls
- machine: darwin-arm64
- commit hash: 04318d0
- commit date: 2025-10-24
- overall geometric mean: 1.027x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 118 ms                                                                   | 114 ms: 1.04x faster                                                   |
| docutils       | 1.06 sec                                                                 | 1.04 sec: 1.03x faster                                                 |
| html5lib       | 23.8 ms                                                                  | 23.0 ms: 1.04x faster                                                  |
| sphinx         | 409 ms                                                                   | 402 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                                    | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager                 | 44.3 ms                                                                  | 42.6 ms: 1.04x faster                                                  |
| async_tree_none                  | 104 ms                                                                   | 101 ms: 1.03x faster                                                   |
| async_tree_eager_tg              | 84.7 ms                                                                  | 82.3 ms: 1.03x faster                                                  |
| async_tree_none_tg               | 103 ms                                                                   | 100.0 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed          | 258 ms                                                                   | 252 ms: 1.02x faster                                                   |
| async_tree_eager_io_tg           | 232 ms                                                                   | 227 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 246 ms                                                                   | 240 ms: 1.02x faster                                                   |
| async_generators                 | 180 ms                                                                   | 176 ms: 1.02x faster                                                   |
| async_tree_io                    | 233 ms                                                                   | 228 ms: 1.02x faster                                                   |
| coroutines                       | 10.3 ms                                                                  | 10.1 ms: 1.02x faster                                                  |
| async_tree_eager_memoization_tg  | 128 ms                                                                   | 126 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 226 ms                                                                   | 222 ms: 1.02x faster                                                   |
| async_tree_memoization           | 144 ms                                                                   | 142 ms: 1.02x faster                                                   |
| async_tree_eager_io              | 232 ms                                                                   | 228 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 258 ms                                                                   | 253 ms: 1.02x faster                                                   |
| async_tree_memoization_tg        | 142 ms                                                                   | 140 ms: 1.02x faster                                                   |
| asyncio_websockets               | 189 ms                                                                   | 186 ms: 1.01x faster                                                   |
| Geometric mean                   | (ref)                                                                    | 1.02x faster                                                           |

Benchmark hidden because not significant (2): async_tree_io_tg, async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 30.7 ms                                                                  | 28.8 ms: 1.07x faster                                                  |
| nbody          | 52.2 ms                                                                  | 49.6 ms: 1.05x faster                                                  |
| pidigits       | 168 ms                                                                   | 163 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 50.7 ms                                                                  | 49.2 ms: 1.03x faster                                                  |
| regex_effbot   | 1.44 ms                                                                  | 1.42 ms: 1.01x faster                                                  |
| regex_v8       | 9.84 ms                                                                  | 9.76 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 967 ms                                                                   | 899 ms: 1.08x faster                                                   |
| pickle_pure_python   | 152 us                                                                   | 147 us: 1.04x faster                                                   |
| xml_etree_process    | 25.7 ms                                                                  | 25.0 ms: 1.03x faster                                                  |
| xml_etree_parse      | 63.9 ms                                                                  | 62.5 ms: 1.02x faster                                                  |
| xml_etree_generate   | 35.7 ms                                                                  | 35.0 ms: 1.02x faster                                                  |
| json_dumps           | 4.03 ms                                                                  | 3.96 ms: 1.02x faster                                                  |
| unpickle_pure_python | 103 us                                                                   | 101 us: 1.02x faster                                                   |
| xml_etree_iterparse  | 40.3 ms                                                                  | 39.7 ms: 1.02x faster                                                  |
| Geometric mean       | (ref)                                                                    | 1.03x faster                                                           |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.35 ms                                                                  | 6.25 ms: 1.02x faster                                                  |
| python_startup         | 8.90 ms                                                                  | 8.81 ms: 1.01x faster                                                  |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                                  | 9.90 ms: 1.06x faster                                                  |
| genshi_xml      | 23.1 ms                                                                  | 22.0 ms: 1.05x faster                                                  |
| django_template | 16.1 ms                                                                  | 15.6 ms: 1.03x faster                                                  |
| mako            | 4.94 ms                                                                  | 4.79 ms: 1.03x faster                                                  |
| Geometric mean  | (ref)                                                                    | 1.04x faster                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads                      | 967 ms                                                                   | 899 ms: 1.08x faster                                                   |
| float                            | 30.7 ms                                                                  | 28.8 ms: 1.07x faster                                                  |
| scimark_sor                      | 52.8 ms                                                                  | 49.6 ms: 1.06x faster                                                  |
| scimark_lu                       | 50.7 ms                                                                  | 47.6 ms: 1.06x faster                                                  |
| scimark_monte_carlo              | 31.0 ms                                                                  | 29.2 ms: 1.06x faster                                                  |
| fannkuch                         | 196 ms                                                                   | 185 ms: 1.06x faster                                                   |
| scimark_fft                      | 132 ms                                                                   | 125 ms: 1.06x faster                                                   |
| genshi_text                      | 10.5 ms                                                                  | 9.90 ms: 1.06x faster                                                  |
| nbody                            | 52.2 ms                                                                  | 49.6 ms: 1.05x faster                                                  |
| genshi_xml                       | 23.1 ms                                                                  | 22.0 ms: 1.05x faster                                                  |
| hexiom                           | 2.95 ms                                                                  | 2.82 ms: 1.05x faster                                                  |
| deepcopy_memo                    | 12.5 us                                                                  | 12.0 us: 1.04x faster                                                  |
| comprehensions                   | 7.77 us                                                                  | 7.44 us: 1.04x faster                                                  |
| chaos                            | 27.5 ms                                                                  | 26.3 ms: 1.04x faster                                                  |
| bpe_tokeniser                    | 2.08 sec                                                                 | 2.00 sec: 1.04x faster                                                 |
| go                               | 58.8 ms                                                                  | 56.5 ms: 1.04x faster                                                  |
| async_tree_eager                 | 44.3 ms                                                                  | 42.6 ms: 1.04x faster                                                  |
| richards_super                   | 25.2 ms                                                                  | 24.2 ms: 1.04x faster                                                  |
| 2to3                             | 118 ms                                                                   | 114 ms: 1.04x faster                                                   |
| generators                       | 18.7 ms                                                                  | 18.0 ms: 1.04x faster                                                  |
| pyflate                          | 201 ms                                                                   | 193 ms: 1.04x faster                                                   |
| sqlglot_v2_parse                 | 573 us                                                                   | 552 us: 1.04x faster                                                   |
| pprint_safe_repr                 | 338 ms                                                                   | 326 ms: 1.04x faster                                                   |
| richards                         | 22.1 ms                                                                  | 21.4 ms: 1.04x faster                                                  |
| pickle_pure_python               | 152 us                                                                   | 147 us: 1.04x faster                                                   |
| html5lib                         | 23.8 ms                                                                  | 23.0 ms: 1.04x faster                                                  |
| logging_simple                   | 2.43 us                                                                  | 2.35 us: 1.03x faster                                                  |
| pprint_pformat                   | 684 ms                                                                   | 661 ms: 1.03x faster                                                   |
| telco                            | 3.01 ms                                                                  | 2.91 ms: 1.03x faster                                                  |
| deepcopy                         | 114 us                                                                   | 110 us: 1.03x faster                                                   |
| raytrace                         | 122 ms                                                                   | 118 ms: 1.03x faster                                                   |
| sqlglot_v2_transpile             | 699 us                                                                   | 677 us: 1.03x faster                                                   |
| subparsers                       | 18.6 ms                                                                  | 18.0 ms: 1.03x faster                                                  |
| meteor_contest                   | 51.3 ms                                                                  | 49.7 ms: 1.03x faster                                                  |
| regex_compile                    | 50.7 ms                                                                  | 49.2 ms: 1.03x faster                                                  |
| create_gc_cycles                 | 943 us                                                                   | 915 us: 1.03x faster                                                   |
| django_template                  | 16.1 ms                                                                  | 15.6 ms: 1.03x faster                                                  |
| mako                             | 4.94 ms                                                                  | 4.79 ms: 1.03x faster                                                  |
| pidigits                         | 168 ms                                                                   | 163 ms: 1.03x faster                                                   |
| deepcopy_reduce                  | 1.19 us                                                                  | 1.15 us: 1.03x faster                                                  |
| nqueens                          | 41.0 ms                                                                  | 39.8 ms: 1.03x faster                                                  |
| async_tree_none                  | 104 ms                                                                   | 101 ms: 1.03x faster                                                   |
| async_tree_eager_tg              | 84.7 ms                                                                  | 82.3 ms: 1.03x faster                                                  |
| async_tree_none_tg               | 103 ms                                                                   | 100.0 ms: 1.03x faster                                                 |
| logging_silent                   | 43.1 ns                                                                  | 42.0 ns: 1.03x faster                                                  |
| xml_etree_process                | 25.7 ms                                                                  | 25.0 ms: 1.03x faster                                                  |
| many_optionals                   | 378 us                                                                   | 368 us: 1.03x faster                                                   |
| docutils                         | 1.06 sec                                                                 | 1.04 sec: 1.03x faster                                                 |
| scimark_sparse_mat_mult          | 1.91 ms                                                                  | 1.86 ms: 1.03x faster                                                  |
| mdp                              | 553 ms                                                                   | 540 ms: 1.03x faster                                                   |
| logging_format                   | 2.65 us                                                                  | 2.58 us: 1.03x faster                                                  |
| crypto_pyaes                     | 38.5 ms                                                                  | 37.6 ms: 1.03x faster                                                  |
| dulwich_log                      | 19.8 ms                                                                  | 19.3 ms: 1.02x faster                                                  |
| sympy_str                        | 105 ms                                                                   | 102 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed          | 258 ms                                                                   | 252 ms: 1.02x faster                                                   |
| async_tree_eager_io_tg           | 232 ms                                                                   | 227 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 246 ms                                                                   | 240 ms: 1.02x faster                                                   |
| xml_etree_parse                  | 63.9 ms                                                                  | 62.5 ms: 1.02x faster                                                  |
| async_generators                 | 180 ms                                                                   | 176 ms: 1.02x faster                                                   |
| sympy_expand                     | 178 ms                                                                   | 174 ms: 1.02x faster                                                   |
| async_tree_io                    | 233 ms                                                                   | 228 ms: 1.02x faster                                                   |
| coroutines                       | 10.3 ms                                                                  | 10.1 ms: 1.02x faster                                                  |
| thrift                           | 322 us                                                                   | 315 us: 1.02x faster                                                   |
| async_tree_eager_memoization_tg  | 128 ms                                                                   | 126 ms: 1.02x faster                                                   |
| sqlglot_v2_optimize              | 23.9 ms                                                                  | 23.4 ms: 1.02x faster                                                  |
| spectral_norm                    | 44.6 ms                                                                  | 43.7 ms: 1.02x faster                                                  |
| xml_etree_generate               | 35.7 ms                                                                  | 35.0 ms: 1.02x faster                                                  |
| json_dumps                       | 4.03 ms                                                                  | 3.96 ms: 1.02x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 226 ms                                                                   | 222 ms: 1.02x faster                                                   |
| async_tree_memoization           | 144 ms                                                                   | 142 ms: 1.02x faster                                                   |
| sqlglot_v2_normalize             | 48.9 ms                                                                  | 48.0 ms: 1.02x faster                                                  |
| json                             | 1.98 ms                                                                  | 1.94 ms: 1.02x faster                                                  |
| gc_traversal                     | 2.10 ms                                                                  | 2.06 ms: 1.02x faster                                                  |
| async_tree_eager_io              | 232 ms                                                                   | 228 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 258 ms                                                                   | 253 ms: 1.02x faster                                                   |
| async_tree_memoization_tg        | 142 ms                                                                   | 140 ms: 1.02x faster                                                   |
| sphinx                           | 409 ms                                                                   | 402 ms: 1.02x faster                                                   |
| bench_mp_pool                    | 42.1 ms                                                                  | 41.4 ms: 1.02x faster                                                  |
| sympy_sum                        | 57.9 ms                                                                  | 57.0 ms: 1.02x faster                                                  |
| unpickle_pure_python             | 103 us                                                                   | 101 us: 1.02x faster                                                   |
| xml_etree_iterparse              | 40.3 ms                                                                  | 39.7 ms: 1.02x faster                                                  |
| python_startup_no_site           | 6.35 ms                                                                  | 6.25 ms: 1.02x faster                                                  |
| deltablue                        | 1.52 ms                                                                  | 1.50 ms: 1.02x faster                                                  |
| sympy_integrate                  | 7.64 ms                                                                  | 7.53 ms: 1.01x faster                                                  |
| asyncio_websockets               | 189 ms                                                                   | 186 ms: 1.01x faster                                                   |
| regex_effbot                     | 1.44 ms                                                                  | 1.42 ms: 1.01x faster                                                  |
| k_core                           | 913 ms                                                                   | 900 ms: 1.01x faster                                                   |
| pycparser                        | 490 ms                                                                   | 484 ms: 1.01x faster                                                   |
| typing_runtime_protocols         | 66.8 us                                                                  | 65.9 us: 1.01x faster                                                  |
| bench_thread_pool                | 420 us                                                                   | 415 us: 1.01x faster                                                   |
| pathlib                          | 11.1 ms                                                                  | 10.9 ms: 1.01x faster                                                  |
| python_startup                   | 8.90 ms                                                                  | 8.81 ms: 1.01x faster                                                  |
| regex_v8                         | 9.84 ms                                                                  | 9.76 ms: 1.01x faster                                                  |
| Geometric mean                   | (ref)                                                                    | 1.03x faster                                                           |

Benchmark hidden because not significant (10): pylint, async_tree_io_tg, json_loads, connected_components, shortest_path, dask, sqlite_synth, regex_dna, coverage, async_tree_eager_memoization

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.00x