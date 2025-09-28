# Results vs. base

- fork: python
- ref: 48d0d0dd9733eae4935f
- machine: darwin-arm64
- commit hash: 48d0d0d
- commit date: 2025-09-26
- overall geometric mean: 1.006x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                                  | 112 ms: 1.02x faster                                                    |
| docutils       | 1.04 sec                                                                | 1.04 sec: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                   | 1.01x faster                                                            |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_generators                 | 178 ms                                                                  | 173 ms: 1.03x faster                                                    |
| coroutines                       | 10.3 ms                                                                 | 10.1 ms: 1.03x faster                                                   |
| async_tree_none                  | 115 ms                                                                  | 113 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed          | 266 ms                                                                  | 261 ms: 1.02x faster                                                    |
| async_tree_eager_tg              | 88.9 ms                                                                 | 87.5 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 263 ms                                                                  | 259 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 249 ms                                                                  | 245 ms: 1.01x faster                                                    |
| async_tree_none_tg               | 107 ms                                                                  | 106 ms: 1.01x faster                                                    |
| async_tree_eager_io_tg           | 257 ms                                                                  | 254 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 223 ms                                                                  | 220 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 131 ms                                                                  | 130 ms: 1.01x faster                                                    |
| async_tree_eager_io              | 252 ms                                                                  | 249 ms: 1.01x faster                                                    |
| async_tree_eager                 | 42.6 ms                                                                 | 42.2 ms: 1.01x faster                                                   |
| async_tree_memoization           | 150 ms                                                                  | 149 ms: 1.01x faster                                                    |
| async_tree_io                    | 256 ms                                                                  | 254 ms: 1.01x faster                                                    |
| async_tree_eager_memoization     | 111 ms                                                                  | 110 ms: 1.01x faster                                                    |
| async_tree_io_tg                 | 255 ms                                                                  | 253 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                                  | 189 ms: 1.01x faster                                                    |
| Geometric mean                   | (ref)                                                                   | 1.01x faster                                                            |

Benchmark hidden because not significant (1): async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 163 ms                                                                  | 161 ms: 1.01x faster                                                    |
| nbody          | 50.7 ms                                                                 | 50.5 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                                   | 1.00x faster                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 9.99 ms                                                                 | 9.78 ms: 1.02x faster                                                   |
| regex_effbot   | 1.46 ms                                                                 | 1.44 ms: 1.02x faster                                                   |
| regex_dna      | 96.6 ms                                                                 | 95.4 ms: 1.01x faster                                                   |
| regex_compile  | 49.5 ms                                                                 | 49.2 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                   | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|---------------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse | 43.3 ms                                                                 | 42.8 ms: 1.01x faster                                                   |
| json_loads          | 10.8 us                                                                 | 10.7 us: 1.01x faster                                                   |
| json_dumps          | 3.84 ms                                                                 | 3.87 ms: 1.01x slower                                                   |
| xml_etree_generate  | 35.9 ms                                                                 | 36.2 ms: 1.01x slower                                                   |
| xml_etree_process   | 25.4 ms                                                                 | 25.7 ms: 1.01x slower                                                   |
| pickle_pure_python  | 147 us                                                                  | 150 us: 1.02x slower                                                    |
| Geometric mean      | (ref)                                                                   | 1.00x slower                                                            |

Benchmark hidden because not significant (3): xml_etree_parse, unpickle_pure_python, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup | 8.67 ms                                                                 | 8.65 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                                   | 1.00x faster                                                            |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml     | 22.3 ms                                                                 | 21.9 ms: 1.02x faster                                                   |
| genshi_text    | 10.2 ms                                                                 | 10.1 ms: 1.01x faster                                                   |
| mako           | 5.01 ms                                                                 | 5.06 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                   | 1.01x faster                                                            |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                        | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| many_optionals                   | 330 us                                                                  | 319 us: 1.03x faster                                                    |
| comprehensions                   | 7.79 us                                                                 | 7.57 us: 1.03x faster                                                   |
| async_generators                 | 178 ms                                                                  | 173 ms: 1.03x faster                                                    |
| scimark_sparse_mat_mult          | 1.90 ms                                                                 | 1.85 ms: 1.03x faster                                                   |
| typing_runtime_protocols         | 64.8 us                                                                 | 63.1 us: 1.03x faster                                                   |
| coroutines                       | 10.3 ms                                                                 | 10.1 ms: 1.03x faster                                                   |
| subparsers                       | 18.2 ms                                                                 | 17.8 ms: 1.02x faster                                                   |
| async_tree_none                  | 115 ms                                                                  | 113 ms: 1.02x faster                                                    |
| regex_v8                         | 9.99 ms                                                                 | 9.78 ms: 1.02x faster                                                   |
| 2to3                             | 114 ms                                                                  | 112 ms: 1.02x faster                                                    |
| regex_effbot                     | 1.46 ms                                                                 | 1.44 ms: 1.02x faster                                                   |
| bpe_tokeniser                    | 2.01 sec                                                                | 1.98 sec: 1.02x faster                                                  |
| async_tree_cpu_io_mixed          | 266 ms                                                                  | 261 ms: 1.02x faster                                                    |
| genshi_xml                       | 22.3 ms                                                                 | 21.9 ms: 1.02x faster                                                   |
| async_tree_eager_tg              | 88.9 ms                                                                 | 87.5 ms: 1.02x faster                                                   |
| pyflate                          | 201 ms                                                                  | 198 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 263 ms                                                                  | 259 ms: 1.02x faster                                                    |
| nqueens                          | 39.8 ms                                                                 | 39.3 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 249 ms                                                                  | 245 ms: 1.01x faster                                                    |
| async_tree_none_tg               | 107 ms                                                                  | 106 ms: 1.01x faster                                                    |
| async_tree_eager_io_tg           | 257 ms                                                                  | 254 ms: 1.01x faster                                                    |
| genshi_text                      | 10.2 ms                                                                 | 10.1 ms: 1.01x faster                                                   |
| hexiom                           | 2.90 ms                                                                 | 2.86 ms: 1.01x faster                                                   |
| telco                            | 2.90 ms                                                                 | 2.86 ms: 1.01x faster                                                   |
| scimark_lu                       | 49.2 ms                                                                 | 48.6 ms: 1.01x faster                                                   |
| regex_dna                        | 96.6 ms                                                                 | 95.4 ms: 1.01x faster                                                   |
| deltablue                        | 1.52 ms                                                                 | 1.50 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 223 ms                                                                  | 220 ms: 1.01x faster                                                    |
| xml_etree_iterparse              | 43.3 ms                                                                 | 42.8 ms: 1.01x faster                                                   |
| async_tree_eager_memoization_tg  | 131 ms                                                                  | 130 ms: 1.01x faster                                                    |
| async_tree_eager_io              | 252 ms                                                                  | 249 ms: 1.01x faster                                                    |
| async_tree_eager                 | 42.6 ms                                                                 | 42.2 ms: 1.01x faster                                                   |
| bench_mp_pool                    | 42.0 ms                                                                 | 41.5 ms: 1.01x faster                                                   |
| async_tree_memoization           | 150 ms                                                                  | 149 ms: 1.01x faster                                                    |
| go                               | 57.6 ms                                                                 | 57.0 ms: 1.01x faster                                                   |
| sympy_integrate                  | 7.44 ms                                                                 | 7.36 ms: 1.01x faster                                                   |
| sympy_str                        | 99.9 ms                                                                 | 98.8 ms: 1.01x faster                                                   |
| pidigits                         | 163 ms                                                                  | 161 ms: 1.01x faster                                                    |
| async_tree_io                    | 256 ms                                                                  | 254 ms: 1.01x faster                                                    |
| sympy_sum                        | 55.9 ms                                                                 | 55.4 ms: 1.01x faster                                                   |
| async_tree_eager_memoization     | 111 ms                                                                  | 110 ms: 1.01x faster                                                    |
| meteor_contest                   | 49.7 ms                                                                 | 49.2 ms: 1.01x faster                                                   |
| logging_format                   | 2.59 us                                                                 | 2.57 us: 1.01x faster                                                   |
| dulwich_log                      | 18.1 ms                                                                 | 18.0 ms: 1.01x faster                                                   |
| logging_simple                   | 2.37 us                                                                 | 2.35 us: 1.01x faster                                                   |
| crypto_pyaes                     | 37.4 ms                                                                 | 37.1 ms: 1.01x faster                                                   |
| async_tree_io_tg                 | 255 ms                                                                  | 253 ms: 1.01x faster                                                    |
| docutils                         | 1.04 sec                                                                | 1.04 sec: 1.01x faster                                                  |
| json_loads                       | 10.8 us                                                                 | 10.7 us: 1.01x faster                                                   |
| json                             | 1.90 ms                                                                 | 1.89 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                                  | 189 ms: 1.01x faster                                                    |
| mdp                              | 546 ms                                                                  | 543 ms: 1.01x faster                                                    |
| regex_compile                    | 49.5 ms                                                                 | 49.2 ms: 1.01x faster                                                   |
| bench_thread_pool                | 426 us                                                                  | 423 us: 1.01x faster                                                    |
| sympy_expand                     | 170 ms                                                                  | 169 ms: 1.01x faster                                                    |
| coverage                         | 32.9 ms                                                                 | 32.7 ms: 1.01x faster                                                   |
| nbody                            | 50.7 ms                                                                 | 50.5 ms: 1.00x faster                                                   |
| sqlglot_v2_optimize              | 23.2 ms                                                                 | 23.1 ms: 1.00x faster                                                   |
| python_startup                   | 8.67 ms                                                                 | 8.65 ms: 1.00x faster                                                   |
| generators                       | 17.4 ms                                                                 | 17.5 ms: 1.00x slower                                                   |
| create_gc_cycles                 | 920 us                                                                  | 924 us: 1.00x slower                                                    |
| richards_super                   | 24.4 ms                                                                 | 24.5 ms: 1.00x slower                                                   |
| json_dumps                       | 3.84 ms                                                                 | 3.87 ms: 1.01x slower                                                   |
| richards                         | 21.5 ms                                                                 | 21.6 ms: 1.01x slower                                                   |
| thrift                           | 312 us                                                                  | 315 us: 1.01x slower                                                    |
| pprint_safe_repr                 | 333 ms                                                                  | 336 ms: 1.01x slower                                                    |
| mako                             | 5.01 ms                                                                 | 5.06 ms: 1.01x slower                                                   |
| xml_etree_generate               | 35.9 ms                                                                 | 36.2 ms: 1.01x slower                                                   |
| shortest_path                    | 218 ms                                                                  | 220 ms: 1.01x slower                                                    |
| scimark_monte_carlo              | 30.3 ms                                                                 | 30.7 ms: 1.01x slower                                                   |
| xml_etree_process                | 25.4 ms                                                                 | 25.7 ms: 1.01x slower                                                   |
| scimark_fft                      | 127 ms                                                                  | 129 ms: 1.01x slower                                                    |
| logging_silent                   | 41.2 ns                                                                 | 41.7 ns: 1.01x slower                                                   |
| chaos                            | 26.5 ms                                                                 | 27.0 ms: 1.02x slower                                                   |
| fannkuch                         | 186 ms                                                                  | 189 ms: 1.02x slower                                                    |
| spectral_norm                    | 43.8 ms                                                                 | 44.6 ms: 1.02x slower                                                   |
| pickle_pure_python               | 147 us                                                                  | 150 us: 1.02x slower                                                    |
| raytrace                         | 119 ms                                                                  | 121 ms: 1.02x slower                                                    |
| Geometric mean                   | (ref)                                                                   | 1.01x faster                                                            |

Benchmark hidden because not significant (25): async_tree_memoization_tg, pylint, sqlite_synth, deepcopy, scimark_sor, sphinx, django_template, sqlglot_v2_normalize, pycparser, deepcopy_memo, xml_etree_parse, sqlglot_v2_parse, gc_traversal, float, unpickle_pure_python, python_startup_no_site, connected_components, html5lib, dask, deepcopy_reduce, k_core, pathlib, pprint_pformat, sqlglot_v2_transpile, tomli_loads
Ignored benchmarks (8) of results/bm-20250926-3.15.0a0-48d0d0d/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.006x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x