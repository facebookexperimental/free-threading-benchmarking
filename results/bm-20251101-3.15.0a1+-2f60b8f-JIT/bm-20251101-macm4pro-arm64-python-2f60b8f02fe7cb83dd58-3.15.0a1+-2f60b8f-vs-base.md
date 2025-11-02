# Results vs. base

- fork: python
- ref: 2f60b8f02fe7cb83dd58
- machine: darwin-arm64
- commit hash: 2f60b8f
- commit date: 2025-11-01
- overall geometric mean: 1.011x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20251101-3.15.0a1+-2f60b8f/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json | results/bm-20251101-3.15.0a1+-2f60b8f-JIT/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json |
|----------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 115 ms                                                                                                              | 118 ms: 1.03x slower                                                                                                    |
| html5lib       | 22.8 ms                                                                                                             | 23.2 ms: 1.02x slower                                                                                                   |
| sphinx         | 402 ms                                                                                                              | 406 ms: 1.01x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                               | 1.02x slower                                                                                                            |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20251101-3.15.0a1+-2f60b8f/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json | results/bm-20251101-3.15.0a1+-2f60b8f-JIT/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json |
|----------------------------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_eager_memoization     | 110 ms                                                                                                              | 108 ms: 1.02x faster                                                                                                    |
| async_tree_eager_cpu_io_mixed_tg | 241 ms                                                                                                              | 244 ms: 1.01x slower                                                                                                    |
| async_tree_eager                 | 42.6 ms                                                                                                             | 43.3 ms: 1.02x slower                                                                                                   |
| async_tree_io                    | 229 ms                                                                                                              | 233 ms: 1.02x slower                                                                                                    |
| coroutines                       | 10.1 ms                                                                                                             | 10.4 ms: 1.03x slower                                                                                                   |
| async_tree_io_tg                 | 226 ms                                                                                                              | 234 ms: 1.03x slower                                                                                                    |
| async_generators                 | 176 ms                                                                                                              | 186 ms: 1.06x slower                                                                                                    |
| Geometric mean                   | (ref)                                                                                                               | 1.00x slower                                                                                                            |

Benchmark hidden because not significant (14): async_tree_none_tg, async_tree_eager_memoization_tg, async_tree_eager_io, asyncio_tcp, async_tree_cpu_io_mixed_tg, async_tree_eager_io_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed, asyncio_websockets, async_tree_memoization, asyncio_tcp_ssl, async_tree_none, async_tree_eager_cpu_io_mixed, async_tree_eager_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20251101-3.15.0a1+-2f60b8f/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json | results/bm-20251101-3.15.0a1+-2f60b8f-JIT/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json |
|----------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 161 ms                                                                                                              | 164 ms: 1.01x slower                                                                                                    |
| float          | 28.2 ms                                                                                                             | 30.2 ms: 1.07x slower                                                                                                   |
| nbody          | 47.9 ms                                                                                                             | 54.1 ms: 1.13x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                               | 1.07x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20251101-3.15.0a1+-2f60b8f/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json | results/bm-20251101-3.15.0a1+-2f60b8f-JIT/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json |
|----------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 48.2 ms                                                                                                             | 48.7 ms: 1.01x slower                                                                                                   |
| regex_dna      | 94.8 ms                                                                                                             | 96.5 ms: 1.02x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                               | 1.01x slower                                                                                                            |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20251101-3.15.0a1+-2f60b8f/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json | results/bm-20251101-3.15.0a1+-2f60b8f-JIT/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json |
|----------------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 889 ms                                                                                                              | 823 ms: 1.08x faster                                                                                                    |
| unpickle_pure_python | 100 us                                                                                                              | 94.2 us: 1.07x faster                                                                                                   |
| xml_etree_process    | 25.4 ms                                                                                                             | 23.9 ms: 1.06x faster                                                                                                   |
| pickle_list          | 2.28 us                                                                                                             | 2.16 us: 1.06x faster                                                                                                   |
| pickle_dict          | 13.7 us                                                                                                             | 13.0 us: 1.05x faster                                                                                                   |
| xml_etree_generate   | 35.8 ms                                                                                                             | 34.2 ms: 1.05x faster                                                                                                   |
| xml_etree_parse      | 62.7 ms                                                                                                             | 61.8 ms: 1.01x faster                                                                                                   |
| pickle               | 6.05 us                                                                                                             | 6.01 us: 1.01x faster                                                                                                   |
| json_dumps           | 3.92 ms                                                                                                             | 3.94 ms: 1.01x slower                                                                                                   |
| unpickle_list        | 2.04 us                                                                                                             | 2.07 us: 1.01x slower                                                                                                   |
| json_loads           | 10.9 us                                                                                                             | 11.1 us: 1.02x slower                                                                                                   |
| unpickle             | 6.25 us                                                                                                             | 6.40 us: 1.03x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                               | 1.02x faster                                                                                                            |

Benchmark hidden because not significant (2): pickle_pure_python, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20251101-3.15.0a1+-2f60b8f/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json | results/bm-20251101-3.15.0a1+-2f60b8f-JIT/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json |
|------------------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 8.75 ms                                                                                                             | 8.90 ms: 1.02x slower                                                                                                   |
| python_startup_no_site | 6.19 ms                                                                                                             | 6.41 ms: 1.03x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                               | 1.03x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20251101-3.15.0a1+-2f60b8f/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json | results/bm-20251101-3.15.0a1+-2f60b8f-JIT/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json |
|-----------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| mako            | 4.81 ms                                                                                                             | 4.38 ms: 1.10x faster                                                                                                   |
| django_template | 15.5 ms                                                                                                             | 15.9 ms: 1.02x slower                                                                                                   |
| genshi_xml      | 22.0 ms                                                                                                             | 22.5 ms: 1.02x slower                                                                                                   |
| genshi_text     | 10.0 ms                                                                                                             | 10.3 ms: 1.03x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                               | 1.01x faster                                                                                                            |

All benchmarks:
===============

| Benchmark                        | results/bm-20251101-3.15.0a1+-2f60b8f/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json | results/bm-20251101-3.15.0a1+-2f60b8f-JIT/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json |
|----------------------------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pprint_safe_repr                 | 326 ms                                                                                                              | 288 ms: 1.13x faster                                                                                                    |
| pprint_pformat                   | 658 ms                                                                                                              | 584 ms: 1.13x faster                                                                                                    |
| mako                             | 4.81 ms                                                                                                             | 4.38 ms: 1.10x faster                                                                                                   |
| tomli_loads                      | 889 ms                                                                                                              | 823 ms: 1.08x faster                                                                                                    |
| unpickle_pure_python             | 100 us                                                                                                              | 94.2 us: 1.07x faster                                                                                                   |
| xml_etree_process                | 25.4 ms                                                                                                             | 23.9 ms: 1.06x faster                                                                                                   |
| pickle_list                      | 2.28 us                                                                                                             | 2.16 us: 1.06x faster                                                                                                   |
| pickle_dict                      | 13.7 us                                                                                                             | 13.0 us: 1.05x faster                                                                                                   |
| telco                            | 2.88 ms                                                                                                             | 2.74 ms: 1.05x faster                                                                                                   |
| xml_etree_generate               | 35.8 ms                                                                                                             | 34.2 ms: 1.05x faster                                                                                                   |
| fannkuch                         | 183 ms                                                                                                              | 179 ms: 1.02x faster                                                                                                    |
| async_tree_eager_memoization     | 110 ms                                                                                                              | 108 ms: 1.02x faster                                                                                                    |
| richards                         | 21.8 ms                                                                                                             | 21.4 ms: 1.02x faster                                                                                                   |
| xml_etree_parse                  | 62.7 ms                                                                                                             | 61.8 ms: 1.01x faster                                                                                                   |
| subparsers                       | 18.1 ms                                                                                                             | 17.9 ms: 1.01x faster                                                                                                   |
| sqlite_synth                     | 972 ns                                                                                                              | 961 ns: 1.01x faster                                                                                                    |
| comprehensions                   | 7.46 us                                                                                                             | 7.40 us: 1.01x faster                                                                                                   |
| pickle                           | 6.05 us                                                                                                             | 6.01 us: 1.01x faster                                                                                                   |
| richards_super                   | 24.5 ms                                                                                                             | 24.3 ms: 1.01x faster                                                                                                   |
| meteor_contest                   | 49.8 ms                                                                                                             | 49.7 ms: 1.00x faster                                                                                                   |
| json_dumps                       | 3.92 ms                                                                                                             | 3.94 ms: 1.01x slower                                                                                                   |
| gc_traversal                     | 2.05 ms                                                                                                             | 2.07 ms: 1.01x slower                                                                                                   |
| sqlglot_v2_optimize              | 23.3 ms                                                                                                             | 23.5 ms: 1.01x slower                                                                                                   |
| bpe_tokeniser                    | 2.00 sec                                                                                                            | 2.01 sec: 1.01x slower                                                                                                  |
| typing_runtime_protocols         | 66.0 us                                                                                                             | 66.5 us: 1.01x slower                                                                                                   |
| create_gc_cycles                 | 922 us                                                                                                              | 930 us: 1.01x slower                                                                                                    |
| regex_compile                    | 48.2 ms                                                                                                             | 48.7 ms: 1.01x slower                                                                                                   |
| many_optionals                   | 363 us                                                                                                              | 367 us: 1.01x slower                                                                                                    |
| async_tree_eager_cpu_io_mixed_tg | 241 ms                                                                                                              | 244 ms: 1.01x slower                                                                                                    |
| pathlib                          | 10.8 ms                                                                                                             | 11.0 ms: 1.01x slower                                                                                                   |
| coverage                         | 32.5 ms                                                                                                             | 32.8 ms: 1.01x slower                                                                                                   |
| sqlglot_v2_normalize             | 47.9 ms                                                                                                             | 48.5 ms: 1.01x slower                                                                                                   |
| sphinx                           | 402 ms                                                                                                              | 406 ms: 1.01x slower                                                                                                    |
| bench_thread_pool                | 414 us                                                                                                              | 419 us: 1.01x slower                                                                                                    |
| pidigits                         | 161 ms                                                                                                              | 164 ms: 1.01x slower                                                                                                    |
| pyflate                          | 189 ms                                                                                                              | 191 ms: 1.01x slower                                                                                                    |
| unpickle_list                    | 2.04 us                                                                                                             | 2.07 us: 1.01x slower                                                                                                   |
| async_tree_eager                 | 42.6 ms                                                                                                             | 43.3 ms: 1.02x slower                                                                                                   |
| crypto_pyaes                     | 37.5 ms                                                                                                             | 38.2 ms: 1.02x slower                                                                                                   |
| python_startup                   | 8.75 ms                                                                                                             | 8.90 ms: 1.02x slower                                                                                                   |
| json_loads                       | 10.9 us                                                                                                             | 11.1 us: 1.02x slower                                                                                                   |
| dulwich_log                      | 19.2 ms                                                                                                             | 19.5 ms: 1.02x slower                                                                                                   |
| html5lib                         | 22.8 ms                                                                                                             | 23.2 ms: 1.02x slower                                                                                                   |
| regex_dna                        | 94.8 ms                                                                                                             | 96.5 ms: 1.02x slower                                                                                                   |
| async_tree_io                    | 229 ms                                                                                                              | 233 ms: 1.02x slower                                                                                                    |
| sympy_sum                        | 56.5 ms                                                                                                             | 57.7 ms: 1.02x slower                                                                                                   |
| json                             | 1.94 ms                                                                                                             | 1.98 ms: 1.02x slower                                                                                                   |
| pycparser                        | 477 ms                                                                                                              | 488 ms: 1.02x slower                                                                                                    |
| sympy_str                        | 103 ms                                                                                                              | 105 ms: 1.02x slower                                                                                                    |
| django_template                  | 15.5 ms                                                                                                             | 15.9 ms: 1.02x slower                                                                                                   |
| genshi_xml                       | 22.0 ms                                                                                                             | 22.5 ms: 1.02x slower                                                                                                   |
| sympy_expand                     | 174 ms                                                                                                              | 179 ms: 1.02x slower                                                                                                    |
| unpickle                         | 6.25 us                                                                                                             | 6.40 us: 1.03x slower                                                                                                   |
| genshi_text                      | 10.0 ms                                                                                                             | 10.3 ms: 1.03x slower                                                                                                   |
| thrift                           | 312 us                                                                                                              | 320 us: 1.03x slower                                                                                                    |
| 2to3                             | 115 ms                                                                                                              | 118 ms: 1.03x slower                                                                                                    |
| coroutines                       | 10.1 ms                                                                                                             | 10.4 ms: 1.03x slower                                                                                                   |
| scimark_sor                      | 48.6 ms                                                                                                             | 50.1 ms: 1.03x slower                                                                                                   |
| logging_format                   | 2.53 us                                                                                                             | 2.60 us: 1.03x slower                                                                                                   |
| logging_simple                   | 2.32 us                                                                                                             | 2.39 us: 1.03x slower                                                                                                   |
| deepcopy_reduce                  | 1.13 us                                                                                                             | 1.17 us: 1.03x slower                                                                                                   |
| deepcopy                         | 108 us                                                                                                              | 111 us: 1.03x slower                                                                                                    |
| mdp                              | 539 ms                                                                                                              | 556 ms: 1.03x slower                                                                                                    |
| spectral_norm                    | 43.1 ms                                                                                                             | 44.6 ms: 1.03x slower                                                                                                   |
| async_tree_io_tg                 | 226 ms                                                                                                              | 234 ms: 1.03x slower                                                                                                    |
| logging_silent                   | 41.8 ns                                                                                                             | 43.2 ns: 1.03x slower                                                                                                   |
| python_startup_no_site           | 6.19 ms                                                                                                             | 6.41 ms: 1.03x slower                                                                                                   |
| sympy_integrate                  | 7.51 ms                                                                                                             | 7.77 ms: 1.03x slower                                                                                                   |
| k_core                           | 902 ms                                                                                                              | 933 ms: 1.03x slower                                                                                                    |
| bench_mp_pool                    | 41.2 ms                                                                                                             | 42.7 ms: 1.04x slower                                                                                                   |
| raytrace                         | 116 ms                                                                                                              | 121 ms: 1.04x slower                                                                                                    |
| hexiom                           | 2.83 ms                                                                                                             | 2.95 ms: 1.04x slower                                                                                                   |
| scimark_monte_carlo              | 28.5 ms                                                                                                             | 29.7 ms: 1.04x slower                                                                                                   |
| nqueens                          | 39.6 ms                                                                                                             | 41.4 ms: 1.05x slower                                                                                                   |
| deepcopy_memo                    | 11.9 us                                                                                                             | 12.4 us: 1.05x slower                                                                                                   |
| shortest_path                    | 226 ms                                                                                                              | 237 ms: 1.05x slower                                                                                                    |
| deltablue                        | 1.46 ms                                                                                                             | 1.53 ms: 1.05x slower                                                                                                   |
| connected_components             | 208 ms                                                                                                              | 219 ms: 1.05x slower                                                                                                    |
| go                               | 54.9 ms                                                                                                             | 57.7 ms: 1.05x slower                                                                                                   |
| chaos                            | 25.4 ms                                                                                                             | 26.8 ms: 1.05x slower                                                                                                   |
| async_generators                 | 176 ms                                                                                                              | 186 ms: 1.06x slower                                                                                                    |
| scimark_lu                       | 47.3 ms                                                                                                             | 50.6 ms: 1.07x slower                                                                                                   |
| float                            | 28.2 ms                                                                                                             | 30.2 ms: 1.07x slower                                                                                                   |
| generators                       | 17.6 ms                                                                                                             | 19.1 ms: 1.09x slower                                                                                                   |
| nbody                            | 47.9 ms                                                                                                             | 54.1 ms: 1.13x slower                                                                                                   |
| scimark_sparse_mat_mult          | 1.75 ms                                                                                                             | 2.00 ms: 1.14x slower                                                                                                   |
| unpack_sequence                  | 28.2 ns                                                                                                             | 32.6 ns: 1.16x slower                                                                                                   |
| Geometric mean                   | (ref)                                                                                                               | 1.01x slower                                                                                                            |

Benchmark hidden because not significant (24): async_tree_none_tg, async_tree_eager_memoization_tg, async_tree_eager_io, asyncio_tcp, async_tree_cpu_io_mixed_tg, async_tree_eager_io_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed, sqlglot_v2_parse, asyncio_websockets, pickle_pure_python, xml_etree_iterparse, dask, sqlglot_v2_transpile, regex_v8, async_tree_memoization, asyncio_tcp_ssl, scimark_fft, async_tree_none, async_tree_eager_cpu_io_mixed, docutils, regex_effbot, async_tree_eager_tg, pylint

- Geometric mean (including insignificant results): 1.011x slower

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x