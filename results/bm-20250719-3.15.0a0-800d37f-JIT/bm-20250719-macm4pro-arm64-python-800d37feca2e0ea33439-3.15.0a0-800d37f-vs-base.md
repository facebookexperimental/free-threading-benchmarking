# Results vs. base

- fork: python
- ref: 800d37feca2e0ea33439
- machine: darwin-arm64
- commit hash: 800d37f
- commit date: 2025-07-19
- overall geometric mean: 1.002x faster
- HPT reliability: 98.37%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250719-3.15.0a0-800d37f/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json | results/bm-20250719-3.15.0a0-800d37f-JIT/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 116 ms                                                                                                            | 120 ms: 1.03x slower                                                                                                  |
| docutils       | 1.07 sec                                                                                                          | 1.09 sec: 1.02x slower                                                                                                |
| html5lib       | 24.6 ms                                                                                                           | 24.9 ms: 1.01x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.02x slower                                                                                                          |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | results/bm-20250719-3.15.0a0-800d37f/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json | results/bm-20250719-3.15.0a0-800d37f-JIT/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json |
|---------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_none_tg              | 112 ms                                                                                                            | 108 ms: 1.04x faster                                                                                                  |
| async_tree_io_tg                | 256 ms                                                                                                            | 254 ms: 1.01x faster                                                                                                  |
| async_tree_eager_cpu_io_mixed   | 226 ms                                                                                                            | 226 ms: 1.00x slower                                                                                                  |
| async_tree_memoization          | 148 ms                                                                                                            | 149 ms: 1.00x slower                                                                                                  |
| async_tree_none                 | 114 ms                                                                                                            | 115 ms: 1.01x slower                                                                                                  |
| async_tree_eager_memoization_tg | 132 ms                                                                                                            | 133 ms: 1.01x slower                                                                                                  |
| async_tree_eager_memoization    | 111 ms                                                                                                            | 113 ms: 1.01x slower                                                                                                  |
| async_tree_eager_io_tg          | 257 ms                                                                                                            | 261 ms: 1.01x slower                                                                                                  |
| async_tree_eager                | 42.4 ms                                                                                                           | 43.1 ms: 1.02x slower                                                                                                 |
| async_tree_eager_io             | 252 ms                                                                                                            | 259 ms: 1.03x slower                                                                                                  |
| coroutines                      | 10.2 ms                                                                                                           | 10.6 ms: 1.04x slower                                                                                                 |
| async_generators                | 178 ms                                                                                                            | 188 ms: 1.06x slower                                                                                                  |
| Geometric mean                  | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (9): asyncio_tcp, asyncio_websockets, async_tree_eager_cpu_io_mixed_tg, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_eager_tg, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250719-3.15.0a0-800d37f/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json | results/bm-20250719-3.15.0a0-800d37f-JIT/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 170 ms                                                                                                            | 169 ms: 1.01x faster                                                                                                  |
| float          | 31.0 ms                                                                                                           | 32.4 ms: 1.05x slower                                                                                                 |
| nbody          | 49.4 ms                                                                                                           | 56.8 ms: 1.15x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.06x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250719-3.15.0a0-800d37f/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json | results/bm-20250719-3.15.0a0-800d37f-JIT/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 10.1 ms                                                                                                           | 9.62 ms: 1.05x faster                                                                                                 |
| regex_dna      | 99.9 ms                                                                                                           | 98.2 ms: 1.02x faster                                                                                                 |
| regex_effbot   | 1.48 ms                                                                                                           | 1.46 ms: 1.02x faster                                                                                                 |
| regex_compile  | 49.5 ms                                                                                                           | 49.0 ms: 1.01x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.02x faster                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250719-3.15.0a0-800d37f/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json | results/bm-20250719-3.15.0a0-800d37f-JIT/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 949 ms                                                                                                            | 828 ms: 1.15x faster                                                                                                  |
| unpickle_pure_python | 101 us                                                                                                            | 91.8 us: 1.10x faster                                                                                                 |
| xml_etree_process    | 25.8 ms                                                                                                           | 24.1 ms: 1.07x faster                                                                                                 |
| xml_etree_parse      | 66.0 ms                                                                                                           | 62.7 ms: 1.05x faster                                                                                                 |
| xml_etree_generate   | 35.9 ms                                                                                                           | 34.5 ms: 1.04x faster                                                                                                 |
| pickle_pure_python   | 148 us                                                                                                            | 144 us: 1.03x faster                                                                                                  |
| xml_etree_iterparse  | 45.9 ms                                                                                                           | 44.5 ms: 1.03x faster                                                                                                 |
| json_dumps           | 4.45 ms                                                                                                           | 4.50 ms: 1.01x slower                                                                                                 |
| pickle_list          | 2.14 us                                                                                                           | 2.16 us: 1.01x slower                                                                                                 |
| unpickle             | 6.42 us                                                                                                           | 6.54 us: 1.02x slower                                                                                                 |
| pickle_dict          | 13.0 us                                                                                                           | 13.7 us: 1.05x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (3): unpickle_list, pickle, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250719-3.15.0a0-800d37f/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json | results/bm-20250719-3.15.0a0-800d37f-JIT/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 8.89 ms                                                                                                           | 8.82 ms: 1.01x faster                                                                                                 |
| python_startup_no_site | 6.34 ms                                                                                                           | 6.29 ms: 1.01x faster                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | results/bm-20250719-3.15.0a0-800d37f/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json | results/bm-20250719-3.15.0a0-800d37f-JIT/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako           | 5.01 ms                                                                                                           | 4.44 ms: 1.13x faster                                                                                                 |
| genshi_text    | 10.2 ms                                                                                                           | 10.2 ms: 1.01x faster                                                                                                 |
| genshi_xml     | 22.4 ms                                                                                                           | 22.3 ms: 1.00x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                       | results/bm-20250719-3.15.0a0-800d37f/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json | results/bm-20250719-3.15.0a0-800d37f-JIT/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json |
|---------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pprint_safe_repr                | 340 ms                                                                                                            | 296 ms: 1.15x faster                                                                                                  |
| tomli_loads                     | 949 ms                                                                                                            | 828 ms: 1.15x faster                                                                                                  |
| pprint_pformat                  | 685 ms                                                                                                            | 598 ms: 1.14x faster                                                                                                  |
| mako                            | 5.01 ms                                                                                                           | 4.44 ms: 1.13x faster                                                                                                 |
| unpickle_pure_python            | 101 us                                                                                                            | 91.8 us: 1.10x faster                                                                                                 |
| xml_etree_process               | 25.8 ms                                                                                                           | 24.1 ms: 1.07x faster                                                                                                 |
| xml_etree_parse                 | 66.0 ms                                                                                                           | 62.7 ms: 1.05x faster                                                                                                 |
| regex_v8                        | 10.1 ms                                                                                                           | 9.62 ms: 1.05x faster                                                                                                 |
| fannkuch                        | 180 ms                                                                                                            | 172 ms: 1.05x faster                                                                                                  |
| telco                           | 3.06 ms                                                                                                           | 2.93 ms: 1.04x faster                                                                                                 |
| xml_etree_generate              | 35.9 ms                                                                                                           | 34.5 ms: 1.04x faster                                                                                                 |
| async_tree_none_tg              | 112 ms                                                                                                            | 108 ms: 1.04x faster                                                                                                  |
| scimark_fft                     | 131 ms                                                                                                            | 127 ms: 1.04x faster                                                                                                  |
| sqlglot_v2_parse                | 583 us                                                                                                            | 563 us: 1.04x faster                                                                                                  |
| pickle_pure_python              | 148 us                                                                                                            | 144 us: 1.03x faster                                                                                                  |
| xml_etree_iterparse             | 45.9 ms                                                                                                           | 44.5 ms: 1.03x faster                                                                                                 |
| scimark_lu                      | 51.2 ms                                                                                                           | 49.7 ms: 1.03x faster                                                                                                 |
| sqlglot_v2_transpile            | 702 us                                                                                                            | 688 us: 1.02x faster                                                                                                  |
| regex_dna                       | 99.9 ms                                                                                                           | 98.2 ms: 1.02x faster                                                                                                 |
| regex_effbot                    | 1.48 ms                                                                                                           | 1.46 ms: 1.02x faster                                                                                                 |
| comprehensions                  | 7.50 us                                                                                                           | 7.41 us: 1.01x faster                                                                                                 |
| create_gc_cycles                | 978 us                                                                                                            | 968 us: 1.01x faster                                                                                                  |
| async_tree_io_tg                | 256 ms                                                                                                            | 254 ms: 1.01x faster                                                                                                  |
| regex_compile                   | 49.5 ms                                                                                                           | 49.0 ms: 1.01x faster                                                                                                 |
| pyflate                         | 198 ms                                                                                                            | 196 ms: 1.01x faster                                                                                                  |
| deepcopy_memo                   | 13.1 us                                                                                                           | 13.0 us: 1.01x faster                                                                                                 |
| sqlite_synth                    | 970 ns                                                                                                            | 962 ns: 1.01x faster                                                                                                  |
| meteor_contest                  | 49.1 ms                                                                                                           | 48.7 ms: 1.01x faster                                                                                                 |
| python_startup                  | 8.89 ms                                                                                                           | 8.82 ms: 1.01x faster                                                                                                 |
| python_startup_no_site          | 6.34 ms                                                                                                           | 6.29 ms: 1.01x faster                                                                                                 |
| sqlglot_v2_optimize             | 23.8 ms                                                                                                           | 23.6 ms: 1.01x faster                                                                                                 |
| gc_traversal                    | 2.13 ms                                                                                                           | 2.12 ms: 1.01x faster                                                                                                 |
| pidigits                        | 170 ms                                                                                                            | 169 ms: 1.01x faster                                                                                                  |
| genshi_text                     | 10.2 ms                                                                                                           | 10.2 ms: 1.01x faster                                                                                                 |
| sqlglot_v2_normalize            | 48.5 ms                                                                                                           | 48.2 ms: 1.01x faster                                                                                                 |
| logging_silent                  | 42.2 ns                                                                                                           | 42.0 ns: 1.00x faster                                                                                                 |
| genshi_xml                      | 22.4 ms                                                                                                           | 22.3 ms: 1.00x faster                                                                                                 |
| async_tree_eager_cpu_io_mixed   | 226 ms                                                                                                            | 226 ms: 1.00x slower                                                                                                  |
| pathlib                         | 11.2 ms                                                                                                           | 11.2 ms: 1.00x slower                                                                                                 |
| generators                      | 19.0 ms                                                                                                           | 19.1 ms: 1.00x slower                                                                                                 |
| bench_mp_pool                   | 45.2 ms                                                                                                           | 45.4 ms: 1.00x slower                                                                                                 |
| bench_thread_pool               | 438 us                                                                                                            | 440 us: 1.00x slower                                                                                                  |
| async_tree_memoization          | 148 ms                                                                                                            | 149 ms: 1.00x slower                                                                                                  |
| async_tree_none                 | 114 ms                                                                                                            | 115 ms: 1.01x slower                                                                                                  |
| sympy_sum                       | 57.5 ms                                                                                                           | 57.9 ms: 1.01x slower                                                                                                 |
| thrift                          | 311 us                                                                                                            | 314 us: 1.01x slower                                                                                                  |
| scimark_sor                     | 51.2 ms                                                                                                           | 51.6 ms: 1.01x slower                                                                                                 |
| async_tree_eager_memoization_tg | 132 ms                                                                                                            | 133 ms: 1.01x slower                                                                                                  |
| async_tree_eager_memoization    | 111 ms                                                                                                            | 113 ms: 1.01x slower                                                                                                  |
| json_dumps                      | 4.45 ms                                                                                                           | 4.50 ms: 1.01x slower                                                                                                 |
| pickle_list                     | 2.14 us                                                                                                           | 2.16 us: 1.01x slower                                                                                                 |
| html5lib                        | 24.6 ms                                                                                                           | 24.9 ms: 1.01x slower                                                                                                 |
| raytrace                        | 121 ms                                                                                                            | 123 ms: 1.01x slower                                                                                                  |
| async_tree_eager_io_tg          | 257 ms                                                                                                            | 261 ms: 1.01x slower                                                                                                  |
| bpe_tokeniser                   | 1.98 sec                                                                                                          | 2.01 sec: 1.01x slower                                                                                                |
| logging_format                  | 2.65 us                                                                                                           | 2.70 us: 1.02x slower                                                                                                 |
| docutils                        | 1.07 sec                                                                                                          | 1.09 sec: 1.02x slower                                                                                                |
| sympy_str                       | 101 ms                                                                                                            | 103 ms: 1.02x slower                                                                                                  |
| logging_simple                  | 2.45 us                                                                                                           | 2.49 us: 1.02x slower                                                                                                 |
| async_tree_eager                | 42.4 ms                                                                                                           | 43.1 ms: 1.02x slower                                                                                                 |
| richards                        | 22.1 ms                                                                                                           | 22.5 ms: 1.02x slower                                                                                                 |
| unpickle                        | 6.42 us                                                                                                           | 6.54 us: 1.02x slower                                                                                                 |
| richards_super                  | 25.0 ms                                                                                                           | 25.4 ms: 1.02x slower                                                                                                 |
| mdp                             | 524 ms                                                                                                            | 535 ms: 1.02x slower                                                                                                  |
| sympy_integrate                 | 7.63 ms                                                                                                           | 7.79 ms: 1.02x slower                                                                                                 |
| sympy_expand                    | 169 ms                                                                                                            | 173 ms: 1.02x slower                                                                                                  |
| nqueens                         | 39.3 ms                                                                                                           | 40.3 ms: 1.02x slower                                                                                                 |
| k_core                          | 962 ms                                                                                                            | 989 ms: 1.03x slower                                                                                                  |
| async_tree_eager_io             | 252 ms                                                                                                            | 259 ms: 1.03x slower                                                                                                  |
| 2to3                            | 116 ms                                                                                                            | 120 ms: 1.03x slower                                                                                                  |
| chaos                           | 26.7 ms                                                                                                           | 27.6 ms: 1.03x slower                                                                                                 |
| deltablue                       | 1.57 ms                                                                                                           | 1.62 ms: 1.03x slower                                                                                                 |
| many_optionals                  | 251 us                                                                                                            | 261 us: 1.04x slower                                                                                                  |
| coroutines                      | 10.2 ms                                                                                                           | 10.6 ms: 1.04x slower                                                                                                 |
| float                           | 31.0 ms                                                                                                           | 32.4 ms: 1.05x slower                                                                                                 |
| shortest_path                   | 222 ms                                                                                                            | 234 ms: 1.05x slower                                                                                                  |
| pickle_dict                     | 13.0 us                                                                                                           | 13.7 us: 1.05x slower                                                                                                 |
| connected_components            | 206 ms                                                                                                            | 218 ms: 1.06x slower                                                                                                  |
| async_generators                | 178 ms                                                                                                            | 188 ms: 1.06x slower                                                                                                  |
| hexiom                          | 2.84 ms                                                                                                           | 3.04 ms: 1.07x slower                                                                                                 |
| spectral_norm                   | 45.7 ms                                                                                                           | 49.0 ms: 1.07x slower                                                                                                 |
| scimark_sparse_mat_mult         | 1.91 ms                                                                                                           | 2.10 ms: 1.10x slower                                                                                                 |
| unpack_sequence                 | 29.7 ns                                                                                                           | 33.4 ns: 1.13x slower                                                                                                 |
| nbody                           | 49.4 ms                                                                                                           | 56.8 ms: 1.15x slower                                                                                                 |
| Geometric mean                  | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmark hidden because not significant (27): asyncio_tcp, deepcopy_reduce, unpickle_list, deepcopy, typing_runtime_protocols, scimark_monte_carlo, dask, dulwich_log, asyncio_websockets, async_tree_eager_cpu_io_mixed_tg, crypto_pyaes, sphinx, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, django_template, coverage, subparsers, pickle, async_tree_memoization_tg, json_loads, go, async_tree_eager_tg, json, pycparser, pylint, asyncio_tcp_ssl

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 98.37% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x