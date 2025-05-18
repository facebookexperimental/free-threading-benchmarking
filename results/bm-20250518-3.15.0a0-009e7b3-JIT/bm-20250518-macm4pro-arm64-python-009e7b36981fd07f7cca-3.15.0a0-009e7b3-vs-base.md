# Results vs. base

- fork: python
- ref: 009e7b36981fd07f7cca
- machine: darwin-arm64
- commit hash: 009e7b3
- commit date: 2025-05-18
- overall geometric mean: 1.000x faster
- HPT reliability: 58.16%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json | results/bm-20250518-3.15.0a0-009e7b3-JIT/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 115 ms                                                                                                            | 115 ms: 1.01x slower                                                                                                  |
| docutils       | 1.05 sec                                                                                                          | 1.06 sec: 1.00x slower                                                                                                |
| Geometric mean | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json | results/bm-20250518-3.15.0a0-009e7b3-JIT/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| asyncio_tcp_ssl                  | 695 ms                                                                                                            | 676 ms: 1.03x faster                                                                                                  |
| async_tree_none                  | 111 ms                                                                                                            | 109 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg       | 264 ms                                                                                                            | 260 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed          | 267 ms                                                                                                            | 264 ms: 1.01x faster                                                                                                  |
| async_tree_none_tg               | 104 ms                                                                                                            | 103 ms: 1.01x faster                                                                                                  |
| asyncio_websockets               | 192 ms                                                                                                            | 191 ms: 1.01x faster                                                                                                  |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                                                                            | 223 ms: 1.01x faster                                                                                                  |
| async_tree_eager_cpu_io_mixed_tg | 248 ms                                                                                                            | 246 ms: 1.01x faster                                                                                                  |
| async_tree_eager                 | 42.2 ms                                                                                                           | 42.4 ms: 1.00x slower                                                                                                 |
| async_tree_eager_memoization     | 111 ms                                                                                                            | 112 ms: 1.01x slower                                                                                                  |
| coroutines                       | 10.5 ms                                                                                                           | 10.6 ms: 1.01x slower                                                                                                 |
| async_generators                 | 177 ms                                                                                                            | 183 ms: 1.03x slower                                                                                                  |
| Geometric mean                   | (ref)                                                                                                             | 1.00x faster                                                                                                          |

Benchmark hidden because not significant (9): async_tree_eager_io_tg, asyncio_tcp, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_io, async_tree_memoization, async_tree_eager_memoization_tg, async_tree_eager_io

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json | results/bm-20250518-3.15.0a0-009e7b3-JIT/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 164 ms                                                                                                            | 163 ms: 1.01x faster                                                                                                  |
| float          | 29.7 ms                                                                                                           | 31.7 ms: 1.07x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.02x slower                                                                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json | results/bm-20250518-3.15.0a0-009e7b3-JIT/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 102 ms                                                                                                            | 101 ms: 1.01x faster                                                                                                  |
| regex_v8       | 9.99 ms                                                                                                           | 9.87 ms: 1.01x faster                                                                                                 |
| regex_compile  | 48.6 ms                                                                                                           | 48.4 ms: 1.00x faster                                                                                                 |
| regex_effbot   | 1.54 ms                                                                                                           | 1.56 ms: 1.01x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.00x faster                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json | results/bm-20250518-3.15.0a0-009e7b3-JIT/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 960 ms                                                                                                            | 869 ms: 1.11x faster                                                                                                  |
| xml_etree_process    | 25.5 ms                                                                                                           | 23.9 ms: 1.07x faster                                                                                                 |
| unpickle_pure_python | 99.0 us                                                                                                           | 94.0 us: 1.05x faster                                                                                                 |
| xml_etree_generate   | 35.9 ms                                                                                                           | 34.2 ms: 1.05x faster                                                                                                 |
| xml_etree_parse      | 62.8 ms                                                                                                           | 61.1 ms: 1.03x faster                                                                                                 |
| pickle_pure_python   | 144 us                                                                                                            | 142 us: 1.02x faster                                                                                                  |
| json_dumps           | 4.61 ms                                                                                                           | 4.66 ms: 1.01x slower                                                                                                 |
| json_loads           | 11.7 us                                                                                                           | 11.8 us: 1.01x slower                                                                                                 |
| unpickle             | 6.22 us                                                                                                           | 6.45 us: 1.04x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.02x faster                                                                                                          |

Benchmark hidden because not significant (5): pickle, pickle_dict, pickle_list, unpickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json | results/bm-20250518-3.15.0a0-009e7b3-JIT/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 8.54 ms                                                                                                           | 8.56 ms: 1.00x slower                                                                                                 |
| python_startup_no_site | 6.12 ms                                                                                                           | 6.14 ms: 1.00x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json | results/bm-20250518-3.15.0a0-009e7b3-JIT/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako            | 4.80 ms                                                                                                           | 4.37 ms: 1.10x faster                                                                                                 |
| genshi_xml      | 21.7 ms                                                                                                           | 21.8 ms: 1.01x slower                                                                                                 |
| django_template | 15.4 ms                                                                                                           | 15.6 ms: 1.01x slower                                                                                                 |
| genshi_text     | 9.94 ms                                                                                                           | 10.2 ms: 1.02x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                             | 1.01x faster                                                                                                          |

All benchmarks:
===============

| Benchmark                        | results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json | results/bm-20250518-3.15.0a0-009e7b3-JIT/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads                      | 960 ms                                                                                                            | 869 ms: 1.11x faster                                                                                                  |
| mako                             | 4.80 ms                                                                                                           | 4.37 ms: 1.10x faster                                                                                                 |
| pprint_safe_repr                 | 318 ms                                                                                                            | 292 ms: 1.09x faster                                                                                                  |
| pprint_pformat                   | 645 ms                                                                                                            | 598 ms: 1.08x faster                                                                                                  |
| xml_etree_process                | 25.5 ms                                                                                                           | 23.9 ms: 1.07x faster                                                                                                 |
| unpickle_pure_python             | 99.0 us                                                                                                           | 94.0 us: 1.05x faster                                                                                                 |
| xml_etree_generate               | 35.9 ms                                                                                                           | 34.2 ms: 1.05x faster                                                                                                 |
| scimark_fft                      | 136 ms                                                                                                            | 130 ms: 1.04x faster                                                                                                  |
| scimark_sor                      | 52.4 ms                                                                                                           | 50.9 ms: 1.03x faster                                                                                                 |
| telco                            | 3.06 ms                                                                                                           | 2.97 ms: 1.03x faster                                                                                                 |
| asyncio_tcp_ssl                  | 695 ms                                                                                                            | 676 ms: 1.03x faster                                                                                                  |
| xml_etree_parse                  | 62.8 ms                                                                                                           | 61.1 ms: 1.03x faster                                                                                                 |
| meteor_contest                   | 50.8 ms                                                                                                           | 49.7 ms: 1.02x faster                                                                                                 |
| pyflate                          | 197 ms                                                                                                            | 193 ms: 1.02x faster                                                                                                  |
| pickle_pure_python               | 144 us                                                                                                            | 142 us: 1.02x faster                                                                                                  |
| deltablue                        | 1.50 ms                                                                                                           | 1.48 ms: 1.02x faster                                                                                                 |
| async_tree_none                  | 111 ms                                                                                                            | 109 ms: 1.02x faster                                                                                                  |
| regex_dna                        | 102 ms                                                                                                            | 101 ms: 1.01x faster                                                                                                  |
| deepcopy                         | 111 us                                                                                                            | 110 us: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg       | 264 ms                                                                                                            | 260 ms: 1.01x faster                                                                                                  |
| regex_v8                         | 9.99 ms                                                                                                           | 9.87 ms: 1.01x faster                                                                                                 |
| async_tree_cpu_io_mixed          | 267 ms                                                                                                            | 264 ms: 1.01x faster                                                                                                  |
| fannkuch                         | 179 ms                                                                                                            | 177 ms: 1.01x faster                                                                                                  |
| subparsers                       | 9.74 ms                                                                                                           | 9.63 ms: 1.01x faster                                                                                                 |
| async_tree_none_tg               | 104 ms                                                                                                            | 103 ms: 1.01x faster                                                                                                  |
| asyncio_websockets               | 192 ms                                                                                                            | 191 ms: 1.01x faster                                                                                                  |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                                                                            | 223 ms: 1.01x faster                                                                                                  |
| async_tree_eager_cpu_io_mixed_tg | 248 ms                                                                                                            | 246 ms: 1.01x faster                                                                                                  |
| bench_mp_pool                    | 44.0 ms                                                                                                           | 43.6 ms: 1.01x faster                                                                                                 |
| scimark_lu                       | 49.0 ms                                                                                                           | 48.7 ms: 1.01x faster                                                                                                 |
| sqlite_synth                     | 950 ns                                                                                                            | 945 ns: 1.01x faster                                                                                                  |
| pidigits                         | 164 ms                                                                                                            | 163 ms: 1.01x faster                                                                                                  |
| regex_compile                    | 48.6 ms                                                                                                           | 48.4 ms: 1.00x faster                                                                                                 |
| python_startup                   | 8.54 ms                                                                                                           | 8.56 ms: 1.00x slower                                                                                                 |
| richards                         | 21.9 ms                                                                                                           | 21.9 ms: 1.00x slower                                                                                                 |
| python_startup_no_site           | 6.12 ms                                                                                                           | 6.14 ms: 1.00x slower                                                                                                 |
| sympy_sum                        | 56.1 ms                                                                                                           | 56.3 ms: 1.00x slower                                                                                                 |
| many_optionals                   | 248 us                                                                                                            | 249 us: 1.00x slower                                                                                                  |
| go                               | 57.0 ms                                                                                                           | 57.2 ms: 1.00x slower                                                                                                 |
| crypto_pyaes                     | 38.1 ms                                                                                                           | 38.2 ms: 1.00x slower                                                                                                 |
| async_tree_eager                 | 42.2 ms                                                                                                           | 42.4 ms: 1.00x slower                                                                                                 |
| docutils                         | 1.05 sec                                                                                                          | 1.06 sec: 1.00x slower                                                                                                |
| create_gc_cycles                 | 929 us                                                                                                            | 934 us: 1.01x slower                                                                                                  |
| sqlglot_v2_parse                 | 550 us                                                                                                            | 553 us: 1.01x slower                                                                                                  |
| pathlib                          | 11.2 ms                                                                                                           | 11.3 ms: 1.01x slower                                                                                                 |
| 2to3                             | 115 ms                                                                                                            | 115 ms: 1.01x slower                                                                                                  |
| genshi_xml                       | 21.7 ms                                                                                                           | 21.8 ms: 1.01x slower                                                                                                 |
| async_tree_eager_memoization     | 111 ms                                                                                                            | 112 ms: 1.01x slower                                                                                                  |
| richards_super                   | 24.6 ms                                                                                                           | 24.8 ms: 1.01x slower                                                                                                 |
| sqlglot_v2_transpile             | 671 us                                                                                                            | 676 us: 1.01x slower                                                                                                  |
| bpe_tokeniser                    | 1.94 sec                                                                                                          | 1.96 sec: 1.01x slower                                                                                                |
| coroutines                       | 10.5 ms                                                                                                           | 10.6 ms: 1.01x slower                                                                                                 |
| logging_silent                   | 195 ns                                                                                                            | 197 ns: 1.01x slower                                                                                                  |
| sqlglot_v2_normalize             | 47.1 ms                                                                                                           | 47.6 ms: 1.01x slower                                                                                                 |
| json_dumps                       | 4.61 ms                                                                                                           | 4.66 ms: 1.01x slower                                                                                                 |
| json_loads                       | 11.7 us                                                                                                           | 11.8 us: 1.01x slower                                                                                                 |
| nqueens                          | 38.2 ms                                                                                                           | 38.7 ms: 1.01x slower                                                                                                 |
| regex_effbot                     | 1.54 ms                                                                                                           | 1.56 ms: 1.01x slower                                                                                                 |
| django_template                  | 15.4 ms                                                                                                           | 15.6 ms: 1.01x slower                                                                                                 |
| chaos                            | 26.4 ms                                                                                                           | 26.8 ms: 1.02x slower                                                                                                 |
| sqlglot_v2_optimize              | 22.9 ms                                                                                                           | 23.3 ms: 1.02x slower                                                                                                 |
| sympy_str                        | 99.5 ms                                                                                                           | 101 ms: 1.02x slower                                                                                                  |
| comprehensions                   | 7.79 us                                                                                                           | 7.94 us: 1.02x slower                                                                                                 |
| logging_simple                   | 2.55 us                                                                                                           | 2.61 us: 1.02x slower                                                                                                 |
| mdp                              | 524 ms                                                                                                            | 535 ms: 1.02x slower                                                                                                  |
| json                             | 1.95 ms                                                                                                           | 2.00 ms: 1.02x slower                                                                                                 |
| generators                       | 17.3 ms                                                                                                           | 17.7 ms: 1.02x slower                                                                                                 |
| genshi_text                      | 9.94 ms                                                                                                           | 10.2 ms: 1.02x slower                                                                                                 |
| sympy_integrate                  | 7.47 ms                                                                                                           | 7.68 ms: 1.03x slower                                                                                                 |
| sympy_expand                     | 166 ms                                                                                                            | 171 ms: 1.03x slower                                                                                                  |
| pycparser                        | 492 ms                                                                                                            | 507 ms: 1.03x slower                                                                                                  |
| scimark_monte_carlo              | 29.7 ms                                                                                                           | 30.6 ms: 1.03x slower                                                                                                 |
| logging_format                   | 2.77 us                                                                                                           | 2.86 us: 1.03x slower                                                                                                 |
| deepcopy_memo                    | 12.4 us                                                                                                           | 12.8 us: 1.03x slower                                                                                                 |
| async_generators                 | 177 ms                                                                                                            | 183 ms: 1.03x slower                                                                                                  |
| hexiom                           | 2.77 ms                                                                                                           | 2.86 ms: 1.03x slower                                                                                                 |
| unpickle                         | 6.22 us                                                                                                           | 6.45 us: 1.04x slower                                                                                                 |
| k_core                           | 949 ms                                                                                                            | 998 ms: 1.05x slower                                                                                                  |
| scimark_sparse_mat_mult          | 1.99 ms                                                                                                           | 2.10 ms: 1.06x slower                                                                                                 |
| connected_components             | 198 ms                                                                                                            | 211 ms: 1.07x slower                                                                                                  |
| float                            | 29.7 ms                                                                                                           | 31.7 ms: 1.07x slower                                                                                                 |
| shortest_path                    | 214 ms                                                                                                            | 230 ms: 1.07x slower                                                                                                  |
| unpack_sequence                  | 30.4 ns                                                                                                           | 36.2 ns: 1.19x slower                                                                                                 |
| Geometric mean                   | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmark hidden because not significant (28): async_tree_eager_io_tg, asyncio_tcp, async_tree_eager_tg, html5lib, pickle, deepcopy_reduce, coverage, pickle_dict, async_tree_io_tg, async_tree_memoization_tg, gc_traversal, async_tree_io, async_tree_memoization, pickle_list, async_tree_eager_memoization_tg, async_tree_eager_io, raytrace, dulwich_log, unpickle_list, spectral_norm, bench_thread_pool, nbody, thrift, dask, typing_runtime_protocols, xml_etree_iterparse, sphinx, pylint

- Geometric mean (including insignificant results): 1.000x faster

# HPT report

- Reliability score: 58.16% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x