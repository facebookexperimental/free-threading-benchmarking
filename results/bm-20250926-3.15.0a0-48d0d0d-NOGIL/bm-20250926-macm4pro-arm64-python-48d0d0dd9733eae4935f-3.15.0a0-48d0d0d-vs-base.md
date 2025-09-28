# Results vs. base

- fork: python
- ref: 48d0d0dd9733eae4935f
- machine: darwin-arm64
- commit hash: 48d0d0d
- commit date: 2025-09-26
- overall geometric mean: 1.002x slower
- HPT reliability: 99.60%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 120 ms                                                                  | 122 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                   | 1.01x slower                                                            |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_memoization_tg  | 111 ms                                                                  | 112 ms: 1.01x slower                                                    |
| async_tree_eager_io_tg           | 193 ms                                                                  | 194 ms: 1.01x slower                                                    |
| async_tree_memoization_tg        | 123 ms                                                                  | 124 ms: 1.01x slower                                                    |
| async_tree_io_tg                 | 197 ms                                                                  | 198 ms: 1.01x slower                                                    |
| asyncio_websockets               | 184 ms                                                                  | 185 ms: 1.01x slower                                                    |
| async_tree_eager_memoization     | 108 ms                                                                  | 109 ms: 1.01x slower                                                    |
| async_tree_memoization           | 128 ms                                                                  | 130 ms: 1.01x slower                                                    |
| async_tree_io                    | 208 ms                                                                  | 210 ms: 1.01x slower                                                    |
| async_tree_eager_io              | 201 ms                                                                  | 203 ms: 1.01x slower                                                    |
| async_tree_eager_tg              | 77.0 ms                                                                 | 78.0 ms: 1.01x slower                                                   |
| async_tree_none_tg               | 85.4 ms                                                                 | 86.5 ms: 1.01x slower                                                   |
| async_tree_cpu_io_mixed_tg       | 231 ms                                                                  | 234 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 223 ms                                                                  | 226 ms: 1.02x slower                                                    |
| async_generators                 | 179 ms                                                                  | 182 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 218 ms                                                                  | 222 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed          | 238 ms                                                                  | 242 ms: 1.02x slower                                                    |
| async_tree_none                  | 98.4 ms                                                                 | 100 ms: 1.02x slower                                                    |
| async_tree_eager                 | 48.0 ms                                                                 | 48.9 ms: 1.02x slower                                                   |
| Geometric mean                   | (ref)                                                                   | 1.01x slower                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 57.5 ms                                                                 | 56.2 ms: 1.02x faster                                                   |
| pidigits       | 160 ms                                                                  | 160 ms: 1.00x faster                                                    |
| float          | 29.5 ms                                                                 | 29.6 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                                   | 1.01x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 9.25 ms                                                                 | 9.37 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                   | 1.00x slower                                                            |

Benchmark hidden because not significant (3): regex_effbot, regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 38.6 ms                                                                 | 37.3 ms: 1.03x faster                                                   |
| xml_etree_parse      | 59.5 ms                                                                 | 58.5 ms: 1.02x faster                                                   |
| unpickle_pure_python | 112 us                                                                  | 111 us: 1.01x faster                                                    |
| pickle_pure_python   | 152 us                                                                  | 151 us: 1.00x faster                                                    |
| xml_etree_generate   | 36.7 ms                                                                 | 36.9 ms: 1.00x slower                                                   |
| json_loads           | 11.4 us                                                                 | 11.5 us: 1.01x slower                                                   |
| Geometric mean       | (ref)                                                                   | 1.01x faster                                                            |

Benchmark hidden because not significant (3): xml_etree_process, json_dumps, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|------------------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 9.51 ms                                                                 | 9.50 ms: 1.00x faster                                                   |
| python_startup_no_site | 6.91 ms                                                                 | 6.90 ms: 1.00x faster                                                   |
| Geometric mean         | (ref)                                                                   | 1.00x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako           | 5.75 ms                                                                 | 5.70 ms: 1.01x faster                                                   |
| genshi_xml     | 24.0 ms                                                                 | 23.9 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                                   | 1.00x faster                                                            |

Benchmark hidden because not significant (2): django_template, genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| scimark_sparse_mat_mult          | 2.23 ms                                                                 | 2.13 ms: 1.05x faster                                                   |
| xml_etree_iterparse              | 38.6 ms                                                                 | 37.3 ms: 1.03x faster                                                   |
| scimark_lu                       | 56.4 ms                                                                 | 54.9 ms: 1.03x faster                                                   |
| nbody                            | 57.5 ms                                                                 | 56.2 ms: 1.02x faster                                                   |
| create_gc_cycles                 | 482 us                                                                  | 472 us: 1.02x faster                                                    |
| telco                            | 3.11 ms                                                                 | 3.05 ms: 1.02x faster                                                   |
| xml_etree_parse                  | 59.5 ms                                                                 | 58.5 ms: 1.02x faster                                                   |
| gc_traversal                     | 759 us                                                                  | 749 us: 1.01x faster                                                    |
| unpickle_pure_python             | 112 us                                                                  | 111 us: 1.01x faster                                                    |
| json                             | 1.99 ms                                                                 | 1.97 ms: 1.01x faster                                                   |
| generators                       | 18.8 ms                                                                 | 18.7 ms: 1.01x faster                                                   |
| connected_components             | 223 ms                                                                  | 222 ms: 1.01x faster                                                    |
| mako                             | 5.75 ms                                                                 | 5.70 ms: 1.01x faster                                                   |
| pyflate                          | 199 ms                                                                  | 197 ms: 1.01x faster                                                    |
| spectral_norm                    | 51.1 ms                                                                 | 50.8 ms: 1.01x faster                                                   |
| typing_runtime_protocols         | 74.1 us                                                                 | 73.7 us: 1.01x faster                                                   |
| scimark_fft                      | 134 ms                                                                  | 134 ms: 1.01x faster                                                    |
| genshi_xml                       | 24.0 ms                                                                 | 23.9 ms: 1.00x faster                                                   |
| pickle_pure_python               | 152 us                                                                  | 151 us: 1.00x faster                                                    |
| nqueens                          | 43.7 ms                                                                 | 43.6 ms: 1.00x faster                                                   |
| sympy_str                        | 110 ms                                                                  | 110 ms: 1.00x faster                                                    |
| pidigits                         | 160 ms                                                                  | 160 ms: 1.00x faster                                                    |
| python_startup                   | 9.51 ms                                                                 | 9.50 ms: 1.00x faster                                                   |
| python_startup_no_site           | 6.91 ms                                                                 | 6.90 ms: 1.00x faster                                                   |
| sqlglot_v2_optimize              | 24.1 ms                                                                 | 24.2 ms: 1.00x slower                                                   |
| k_core                           | 989 ms                                                                  | 993 ms: 1.00x slower                                                    |
| bench_mp_pool                    | 41.9 ms                                                                 | 42.0 ms: 1.00x slower                                                   |
| float                            | 29.5 ms                                                                 | 29.6 ms: 1.00x slower                                                   |
| xml_etree_generate               | 36.7 ms                                                                 | 36.9 ms: 1.00x slower                                                   |
| async_tree_eager_memoization_tg  | 111 ms                                                                  | 112 ms: 1.01x slower                                                    |
| logging_silent                   | 44.4 ns                                                                 | 44.7 ns: 1.01x slower                                                   |
| sqlglot_v2_parse                 | 595 us                                                                  | 599 us: 1.01x slower                                                    |
| async_tree_eager_io_tg           | 193 ms                                                                  | 194 ms: 1.01x slower                                                    |
| async_tree_memoization_tg        | 123 ms                                                                  | 124 ms: 1.01x slower                                                    |
| async_tree_io_tg                 | 197 ms                                                                  | 198 ms: 1.01x slower                                                    |
| bpe_tokeniser                    | 1.98 sec                                                                | 2.00 sec: 1.01x slower                                                  |
| asyncio_websockets               | 184 ms                                                                  | 185 ms: 1.01x slower                                                    |
| deepcopy_reduce                  | 1.24 us                                                                 | 1.25 us: 1.01x slower                                                   |
| async_tree_eager_memoization     | 108 ms                                                                  | 109 ms: 1.01x slower                                                    |
| chaos                            | 29.2 ms                                                                 | 29.4 ms: 1.01x slower                                                   |
| hexiom                           | 3.13 ms                                                                 | 3.16 ms: 1.01x slower                                                   |
| deepcopy                         | 114 us                                                                  | 115 us: 1.01x slower                                                    |
| subparsers                       | 18.8 ms                                                                 | 19.0 ms: 1.01x slower                                                   |
| richards_super                   | 26.7 ms                                                                 | 27.0 ms: 1.01x slower                                                   |
| async_tree_memoization           | 128 ms                                                                  | 130 ms: 1.01x slower                                                    |
| async_tree_io                    | 208 ms                                                                  | 210 ms: 1.01x slower                                                    |
| richards                         | 23.3 ms                                                                 | 23.6 ms: 1.01x slower                                                   |
| json_loads                       | 11.4 us                                                                 | 11.5 us: 1.01x slower                                                   |
| async_tree_eager_io              | 201 ms                                                                  | 203 ms: 1.01x slower                                                    |
| logging_format                   | 2.76 us                                                                 | 2.79 us: 1.01x slower                                                   |
| async_tree_eager_tg              | 77.0 ms                                                                 | 78.0 ms: 1.01x slower                                                   |
| coverage                         | 40.1 ms                                                                 | 40.6 ms: 1.01x slower                                                   |
| logging_simple                   | 2.46 us                                                                 | 2.49 us: 1.01x slower                                                   |
| deltablue                        | 1.61 ms                                                                 | 1.63 ms: 1.01x slower                                                   |
| regex_v8                         | 9.25 ms                                                                 | 9.37 ms: 1.01x slower                                                   |
| many_optionals                   | 333 us                                                                  | 337 us: 1.01x slower                                                    |
| async_tree_none_tg               | 85.4 ms                                                                 | 86.5 ms: 1.01x slower                                                   |
| async_tree_cpu_io_mixed_tg       | 231 ms                                                                  | 234 ms: 1.01x slower                                                    |
| deepcopy_memo                    | 13.0 us                                                                 | 13.2 us: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 223 ms                                                                  | 226 ms: 1.02x slower                                                    |
| 2to3                             | 120 ms                                                                  | 122 ms: 1.02x slower                                                    |
| go                               | 61.5 ms                                                                 | 62.5 ms: 1.02x slower                                                   |
| comprehensions                   | 8.29 us                                                                 | 8.42 us: 1.02x slower                                                   |
| async_generators                 | 179 ms                                                                  | 182 ms: 1.02x slower                                                    |
| sqlite_synth                     | 821 ns                                                                  | 836 ns: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 218 ms                                                                  | 222 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed          | 238 ms                                                                  | 242 ms: 1.02x slower                                                    |
| async_tree_none                  | 98.4 ms                                                                 | 100 ms: 1.02x slower                                                    |
| async_tree_eager                 | 48.0 ms                                                                 | 48.9 ms: 1.02x slower                                                   |
| Geometric mean                   | (ref)                                                                   | 1.00x slower                                                            |

Benchmark hidden because not significant (34): regex_effbot, mdp, xml_etree_process, raytrace, django_template, pathlib, shortest_path, pprint_safe_repr, pylint, sympy_integrate, coroutines, regex_compile, dask, json_dumps, scimark_monte_carlo, pprint_pformat, genshi_text, sympy_sum, sqlglot_v2_normalize, sphinx, meteor_contest, dulwich_log, crypto_pyaes, thrift, pycparser, sympy_expand, tomli_loads, regex_dna, docutils, sqlglot_v2_transpile, html5lib, bench_thread_pool, fannkuch, scimark_sor
Ignored benchmarks (8) of results/bm-20250926-3.15.0a0-48d0d0d-NOGIL/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 99.60% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x