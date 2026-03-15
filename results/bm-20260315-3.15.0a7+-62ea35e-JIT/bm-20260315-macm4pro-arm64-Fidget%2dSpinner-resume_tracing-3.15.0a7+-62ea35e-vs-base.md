# Results vs. base

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 62ea35e
- commit date: 2026-03-15
- overall geometric mean: 1.042x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7+-788c329 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 116 ms                                                                   | 110 ms: 1.05x faster                                                         |
| docutils       | 1.00 sec                                                                 | 953 ms: 1.05x faster                                                         |
| html5lib       | 20.2 ms                                                                  | 18.7 ms: 1.08x faster                                                        |
| sphinx         | 399 ms                                                                   | 383 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                                    | 1.06x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7+-788c329 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| coroutines                       | 11.1 ms                                                                  | 9.20 ms: 1.21x faster                                                        |
| async_tree_io                    | 228 ms                                                                   | 204 ms: 1.11x faster                                                         |
| async_tree_none_tg               | 97.4 ms                                                                  | 89.0 ms: 1.09x faster                                                        |
| async_tree_none                  | 95.1 ms                                                                  | 87.9 ms: 1.08x faster                                                        |
| async_tree_eager_io_tg           | 218 ms                                                                   | 202 ms: 1.08x faster                                                         |
| async_tree_io_tg                 | 222 ms                                                                   | 207 ms: 1.07x faster                                                         |
| async_tree_eager_tg              | 81.9 ms                                                                  | 76.7 ms: 1.07x faster                                                        |
| async_tree_eager_io              | 218 ms                                                                   | 204 ms: 1.07x faster                                                         |
| async_tree_memoization_tg        | 135 ms                                                                   | 127 ms: 1.06x faster                                                         |
| async_tree_memoization           | 132 ms                                                                   | 126 ms: 1.05x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 247 ms                                                                   | 236 ms: 1.05x faster                                                         |
| async_generators                 | 189 ms                                                                   | 181 ms: 1.05x faster                                                         |
| async_tree_cpu_io_mixed          | 246 ms                                                                   | 235 ms: 1.05x faster                                                         |
| async_tree_eager_memoization_tg  | 120 ms                                                                   | 116 ms: 1.04x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 240 ms                                                                   | 232 ms: 1.04x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 216 ms                                                                   | 210 ms: 1.03x faster                                                         |
| async_tree_eager                 | 37.0 ms                                                                  | 35.9 ms: 1.03x faster                                                        |
| asyncio_websockets               | 188 ms                                                                   | 183 ms: 1.03x faster                                                         |
| async_tree_eager_memoization     | 104 ms                                                                   | 102 ms: 1.01x faster                                                         |
| Geometric mean                   | (ref)                                                                    | 1.06x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7+-788c329 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 164 ms                                                                   | 157 ms: 1.04x faster                                                         |
| float          | 23.6 ms                                                                  | 23.3 ms: 1.02x faster                                                        |
| nbody          | 40.2 ms                                                                  | 39.9 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7+-788c329 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 40.9 ms                                                                  | 39.2 ms: 1.04x faster                                                        |
| regex_dna      | 96.1 ms                                                                  | 92.7 ms: 1.04x faster                                                        |
| regex_v8       | 9.74 ms                                                                  | 9.54 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7+-788c329 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_process    | 22.7 ms                                                                  | 21.2 ms: 1.07x faster                                                        |
| json_loads           | 10.7 us                                                                  | 10.2 us: 1.04x faster                                                        |
| pickle_pure_python   | 129 us                                                                   | 124 us: 1.04x faster                                                         |
| json_dumps           | 3.59 ms                                                                  | 3.48 ms: 1.03x faster                                                        |
| xml_etree_iterparse  | 38.8 ms                                                                  | 37.6 ms: 1.03x faster                                                        |
| tomli_loads          | 636 ms                                                                   | 617 ms: 1.03x faster                                                         |
| unpickle_pure_python | 85.7 us                                                                  | 83.9 us: 1.02x faster                                                        |
| xml_etree_parse      | 59.5 ms                                                                  | 62.3 ms: 1.05x slower                                                        |
| Geometric mean       | (ref)                                                                    | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7+-788c329 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.82 ms                                                                  | 8.64 ms: 1.02x faster                                                        |
| python_startup_no_site | 6.34 ms                                                                  | 6.22 ms: 1.02x faster                                                        |
| Geometric mean         | (ref)                                                                    | 1.02x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7+-788c329 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 14.0 ms                                                                  | 12.3 ms: 1.13x faster                                                        |
| mako            | 3.96 ms                                                                  | 3.97 ms: 1.00x slower                                                        |
| Geometric mean  | (ref)                                                                    | 1.06x faster                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7+-788c329 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| logging_format                   | 2.41 us                                                                  | 1.90 us: 1.27x faster                                                        |
| logging_simple                   | 2.21 us                                                                  | 1.74 us: 1.27x faster                                                        |
| coroutines                       | 11.1 ms                                                                  | 9.20 ms: 1.21x faster                                                        |
| django_template                  | 14.0 ms                                                                  | 12.3 ms: 1.13x faster                                                        |
| async_tree_io                    | 228 ms                                                                   | 204 ms: 1.11x faster                                                         |
| sqlglot_v2_normalize             | 46.6 ms                                                                  | 42.4 ms: 1.10x faster                                                        |
| async_tree_none_tg               | 97.4 ms                                                                  | 89.0 ms: 1.09x faster                                                        |
| sqlglot_v2_optimize              | 22.5 ms                                                                  | 20.8 ms: 1.08x faster                                                        |
| async_tree_none                  | 95.1 ms                                                                  | 87.9 ms: 1.08x faster                                                        |
| deltablue                        | 1.20 ms                                                                  | 1.11 ms: 1.08x faster                                                        |
| html5lib                         | 20.2 ms                                                                  | 18.7 ms: 1.08x faster                                                        |
| async_tree_eager_io_tg           | 218 ms                                                                   | 202 ms: 1.08x faster                                                         |
| chaos                            | 22.3 ms                                                                  | 20.7 ms: 1.08x faster                                                        |
| async_tree_io_tg                 | 222 ms                                                                   | 207 ms: 1.07x faster                                                         |
| xml_etree_process                | 22.7 ms                                                                  | 21.2 ms: 1.07x faster                                                        |
| sqlglot_v2_transpile             | 584 us                                                                   | 546 us: 1.07x faster                                                         |
| many_optionals                   | 237 us                                                                   | 222 us: 1.07x faster                                                         |
| dulwich_log                      | 18.8 ms                                                                  | 17.6 ms: 1.07x faster                                                        |
| async_tree_eager_tg              | 81.9 ms                                                                  | 76.7 ms: 1.07x faster                                                        |
| async_tree_eager_io              | 218 ms                                                                   | 204 ms: 1.07x faster                                                         |
| async_tree_memoization_tg        | 135 ms                                                                   | 127 ms: 1.06x faster                                                         |
| sympy_expand                     | 172 ms                                                                   | 162 ms: 1.06x faster                                                         |
| scimark_sor                      | 38.8 ms                                                                  | 36.6 ms: 1.06x faster                                                        |
| sqlglot_v2_parse                 | 460 us                                                                   | 437 us: 1.05x faster                                                         |
| async_tree_memoization           | 132 ms                                                                   | 126 ms: 1.05x faster                                                         |
| generators                       | 19.2 ms                                                                  | 18.2 ms: 1.05x faster                                                        |
| coverage                         | 34.2 ms                                                                  | 32.5 ms: 1.05x faster                                                        |
| mdp                              | 547 ms                                                                   | 520 ms: 1.05x faster                                                         |
| 2to3                             | 116 ms                                                                   | 110 ms: 1.05x faster                                                         |
| docutils                         | 1.00 sec                                                                 | 953 ms: 1.05x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 247 ms                                                                   | 236 ms: 1.05x faster                                                         |
| thrift                           | 311 us                                                                   | 298 us: 1.05x faster                                                         |
| async_generators                 | 189 ms                                                                   | 181 ms: 1.05x faster                                                         |
| create_gc_cycles                 | 918 us                                                                   | 878 us: 1.05x faster                                                         |
| async_tree_cpu_io_mixed          | 246 ms                                                                   | 235 ms: 1.05x faster                                                         |
| sphinx                           | 399 ms                                                                   | 383 ms: 1.04x faster                                                         |
| regex_compile                    | 40.9 ms                                                                  | 39.2 ms: 1.04x faster                                                        |
| typing_runtime_protocols         | 64.8 us                                                                  | 62.1 us: 1.04x faster                                                        |
| sympy_sum                        | 55.7 ms                                                                  | 53.4 ms: 1.04x faster                                                        |
| pidigits                         | 164 ms                                                                   | 157 ms: 1.04x faster                                                         |
| async_tree_eager_memoization_tg  | 120 ms                                                                   | 116 ms: 1.04x faster                                                         |
| json_loads                       | 10.7 us                                                                  | 10.2 us: 1.04x faster                                                        |
| raytrace                         | 114 ms                                                                   | 110 ms: 1.04x faster                                                         |
| pickle_pure_python               | 129 us                                                                   | 124 us: 1.04x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 240 ms                                                                   | 232 ms: 1.04x faster                                                         |
| gc_traversal                     | 2.05 ms                                                                  | 1.98 ms: 1.04x faster                                                        |
| regex_dna                        | 96.1 ms                                                                  | 92.7 ms: 1.04x faster                                                        |
| pathlib                          | 10.8 ms                                                                  | 10.5 ms: 1.04x faster                                                        |
| deepcopy_reduce                  | 1.03 us                                                                  | 998 ns: 1.03x faster                                                         |
| meteor_contest                   | 45.6 ms                                                                  | 44.2 ms: 1.03x faster                                                        |
| json_dumps                       | 3.59 ms                                                                  | 3.48 ms: 1.03x faster                                                        |
| xml_etree_iterparse              | 38.8 ms                                                                  | 37.6 ms: 1.03x faster                                                        |
| bench_mp_pool                    | 45.1 ms                                                                  | 43.8 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 216 ms                                                                   | 210 ms: 1.03x faster                                                         |
| tomli_loads                      | 636 ms                                                                   | 617 ms: 1.03x faster                                                         |
| subparsers                       | 3.56 ms                                                                  | 3.46 ms: 1.03x faster                                                        |
| async_tree_eager                 | 37.0 ms                                                                  | 35.9 ms: 1.03x faster                                                        |
| pyflate                          | 148 ms                                                                   | 144 ms: 1.03x faster                                                         |
| deepcopy                         | 95.0 us                                                                  | 92.4 us: 1.03x faster                                                        |
| pycparser                        | 452 ms                                                                   | 440 ms: 1.03x faster                                                         |
| pylint                           | 119 ms                                                                   | 116 ms: 1.03x faster                                                         |
| asyncio_websockets               | 188 ms                                                                   | 183 ms: 1.03x faster                                                         |
| sympy_str                        | 102 ms                                                                   | 99.4 ms: 1.03x faster                                                        |
| go                               | 46.6 ms                                                                  | 45.4 ms: 1.03x faster                                                        |
| json                             | 1.84 ms                                                                  | 1.80 ms: 1.02x faster                                                        |
| scimark_monte_carlo              | 23.2 ms                                                                  | 22.7 ms: 1.02x faster                                                        |
| pprint_safe_repr                 | 255 ms                                                                   | 249 ms: 1.02x faster                                                         |
| unpickle_pure_python             | 85.7 us                                                                  | 83.9 us: 1.02x faster                                                        |
| python_startup                   | 8.82 ms                                                                  | 8.64 ms: 1.02x faster                                                        |
| regex_v8                         | 9.74 ms                                                                  | 9.54 ms: 1.02x faster                                                        |
| sqlite_synth                     | 952 ns                                                                   | 933 ns: 1.02x faster                                                         |
| python_startup_no_site           | 6.34 ms                                                                  | 6.22 ms: 1.02x faster                                                        |
| hexiom                           | 2.45 ms                                                                  | 2.40 ms: 1.02x faster                                                        |
| fannkuch                         | 151 ms                                                                   | 148 ms: 1.02x faster                                                         |
| crypto_pyaes                     | 31.9 ms                                                                  | 31.3 ms: 1.02x faster                                                        |
| pprint_pformat                   | 516 ms                                                                   | 507 ms: 1.02x faster                                                         |
| deepcopy_memo                    | 10.1 us                                                                  | 9.98 us: 1.02x faster                                                        |
| float                            | 23.6 ms                                                                  | 23.3 ms: 1.02x faster                                                        |
| scimark_sparse_mat_mult          | 1.85 ms                                                                  | 1.83 ms: 1.01x faster                                                        |
| sympy_integrate                  | 7.57 ms                                                                  | 7.47 ms: 1.01x faster                                                        |
| async_tree_eager_memoization     | 104 ms                                                                   | 102 ms: 1.01x faster                                                         |
| bpe_tokeniser                    | 1.79 sec                                                                 | 1.77 sec: 1.01x faster                                                       |
| comprehensions                   | 5.89 us                                                                  | 5.82 us: 1.01x faster                                                        |
| nbody                            | 40.2 ms                                                                  | 39.9 ms: 1.01x faster                                                        |
| k_core                           | 859 ms                                                                   | 854 ms: 1.01x faster                                                         |
| connected_components             | 196 ms                                                                   | 195 ms: 1.00x faster                                                         |
| mako                             | 3.96 ms                                                                  | 3.97 ms: 1.00x slower                                                        |
| bench_thread_pool                | 430 us                                                                   | 433 us: 1.01x slower                                                         |
| logging_silent                   | 34.4 ns                                                                  | 35.0 ns: 1.02x slower                                                        |
| richards_super                   | 11.2 ms                                                                  | 11.4 ms: 1.02x slower                                                        |
| richards                         | 9.35 ms                                                                  | 9.66 ms: 1.03x slower                                                        |
| xml_etree_parse                  | 59.5 ms                                                                  | 62.3 ms: 1.05x slower                                                        |
| Geometric mean                   | (ref)                                                                    | 1.04x faster                                                                 |

Benchmark hidden because not significant (9): spectral_norm, telco, dask, scimark_fft, xml_etree_generate, shortest_path, nqueens, scimark_lu, regex_effbot
Ignored benchmarks (8) of results/bm-20260314-3.15.0a7+-788c329-JIT/bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7+-788c329.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.042x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.01x