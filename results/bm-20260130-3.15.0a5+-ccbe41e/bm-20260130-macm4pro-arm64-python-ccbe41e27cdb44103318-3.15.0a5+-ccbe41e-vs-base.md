# Results vs. base

- fork: python
- ref: ccbe41e27cdb44103318
- machine: darwin-arm64
- commit hash: ccbe41e
- commit date: 2026-01-30
- overall geometric mean: 1.014x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 107 ms                                                                   | 111 ms: 1.04x slower                                                     |
| docutils       | 972 ms                                                                   | 991 ms: 1.02x slower                                                     |
| html5lib       | 20.7 ms                                                                  | 21.0 ms: 1.01x slower                                                    |
| sphinx         | 377 ms                                                                   | 382 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_memoization     | 104 ms                                                                   | 103 ms: 1.01x faster                                                     |
| async_tree_memoization           | 134 ms                                                                   | 136 ms: 1.01x slower                                                     |
| async_tree_none_tg               | 94.0 ms                                                                  | 95.8 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 116 ms                                                                   | 118 ms: 1.02x slower                                                     |
| asyncio_websockets               | 181 ms                                                                   | 184 ms: 1.02x slower                                                     |
| async_tree_eager                 | 38.8 ms                                                                  | 39.6 ms: 1.02x slower                                                    |
| async_tree_none                  | 98.6 ms                                                                  | 101 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed          | 246 ms                                                                   | 253 ms: 1.03x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 226 ms                                                                   | 232 ms: 1.03x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 211 ms                                                                   | 216 ms: 1.03x slower                                                     |
| async_tree_eager_tg              | 76.8 ms                                                                  | 78.8 ms: 1.03x slower                                                    |
| async_tree_memoization_tg        | 131 ms                                                                   | 135 ms: 1.03x slower                                                     |
| async_tree_cpu_io_mixed_tg       | 240 ms                                                                   | 247 ms: 1.03x slower                                                     |
| async_tree_io                    | 219 ms                                                                   | 226 ms: 1.03x slower                                                     |
| async_tree_eager_io              | 212 ms                                                                   | 219 ms: 1.03x slower                                                     |
| async_tree_io_tg                 | 219 ms                                                                   | 226 ms: 1.03x slower                                                     |
| async_generators                 | 168 ms                                                                   | 175 ms: 1.04x slower                                                     |
| async_tree_eager_io_tg           | 211 ms                                                                   | 221 ms: 1.05x slower                                                     |
| Geometric mean                   | (ref)                                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 43.8 ms                                                                  | 44.1 ms: 1.01x slower                                                    |
| pidigits       | 156 ms                                                                   | 157 ms: 1.01x slower                                                     |
| float          | 27.6 ms                                                                  | 27.9 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 44.1 ms                                                                  | 44.3 ms: 1.00x slower                                                    |
| regex_v8       | 9.39 ms                                                                  | 9.45 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                             |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|---------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_process   | 23.9 ms                                                                  | 24.1 ms: 1.01x slower                                                    |
| xml_etree_iterparse | 39.0 ms                                                                  | 39.8 ms: 1.02x slower                                                    |
| json_dumps          | 3.77 ms                                                                  | 3.84 ms: 1.02x slower                                                    |
| xml_etree_parse     | 60.3 ms                                                                  | 63.4 ms: 1.05x slower                                                    |
| Geometric mean      | (ref)                                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (5): unpickle_pure_python, xml_etree_generate, pickle_pure_python, json_loads, tomli_loads

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|-----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.61 ms                                                                  | 4.54 ms: 1.01x faster                                                    |
| genshi_xml      | 20.4 ms                                                                  | 20.8 ms: 1.02x slower                                                    |
| genshi_text     | 9.43 ms                                                                  | 9.65 ms: 1.02x slower                                                    |
| django_template | 14.2 ms                                                                  | 14.6 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                                    | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako                             | 4.61 ms                                                                  | 4.54 ms: 1.01x faster                                                    |
| scimark_sor                      | 48.8 ms                                                                  | 48.3 ms: 1.01x faster                                                    |
| async_tree_eager_memoization     | 104 ms                                                                   | 103 ms: 1.01x faster                                                     |
| spectral_norm                    | 44.5 ms                                                                  | 44.1 ms: 1.01x faster                                                    |
| telco                            | 2.81 ms                                                                  | 2.79 ms: 1.01x faster                                                    |
| bench_thread_pool                | 430 us                                                                   | 431 us: 1.00x slower                                                     |
| regex_compile                    | 44.1 ms                                                                  | 44.3 ms: 1.00x slower                                                    |
| regex_v8                         | 9.39 ms                                                                  | 9.45 ms: 1.01x slower                                                    |
| sqlglot_v2_parse                 | 497 us                                                                   | 500 us: 1.01x slower                                                     |
| pathlib                          | 10.5 ms                                                                  | 10.6 ms: 1.01x slower                                                    |
| pyflate                          | 185 ms                                                                   | 187 ms: 1.01x slower                                                     |
| json                             | 1.84 ms                                                                  | 1.85 ms: 1.01x slower                                                    |
| nbody                            | 43.8 ms                                                                  | 44.1 ms: 1.01x slower                                                    |
| scimark_monte_carlo              | 27.4 ms                                                                  | 27.6 ms: 1.01x slower                                                    |
| xml_etree_process                | 23.9 ms                                                                  | 24.1 ms: 1.01x slower                                                    |
| sympy_integrate                  | 7.22 ms                                                                  | 7.28 ms: 1.01x slower                                                    |
| sqlglot_v2_transpile             | 611 us                                                                   | 616 us: 1.01x slower                                                     |
| pidigits                         | 156 ms                                                                   | 157 ms: 1.01x slower                                                     |
| gc_traversal                     | 1.97 ms                                                                  | 1.98 ms: 1.01x slower                                                    |
| pprint_pformat                   | 610 ms                                                                   | 616 ms: 1.01x slower                                                     |
| sympy_expand                     | 165 ms                                                                   | 167 ms: 1.01x slower                                                     |
| float                            | 27.6 ms                                                                  | 27.9 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 1.88 ms                                                                  | 1.90 ms: 1.01x slower                                                    |
| fannkuch                         | 166 ms                                                                   | 168 ms: 1.01x slower                                                     |
| richards                         | 19.4 ms                                                                  | 19.6 ms: 1.01x slower                                                    |
| shortest_path                    | 222 ms                                                                   | 225 ms: 1.01x slower                                                     |
| sympy_str                        | 97.6 ms                                                                  | 98.8 ms: 1.01x slower                                                    |
| sphinx                           | 377 ms                                                                   | 382 ms: 1.01x slower                                                     |
| html5lib                         | 20.7 ms                                                                  | 21.0 ms: 1.01x slower                                                    |
| async_tree_memoization           | 134 ms                                                                   | 136 ms: 1.01x slower                                                     |
| go                               | 50.9 ms                                                                  | 51.6 ms: 1.01x slower                                                    |
| connected_components             | 204 ms                                                                   | 207 ms: 1.02x slower                                                     |
| generators                       | 17.8 ms                                                                  | 18.0 ms: 1.02x slower                                                    |
| coverage                         | 30.7 ms                                                                  | 31.2 ms: 1.02x slower                                                    |
| deepcopy_reduce                  | 1.04 us                                                                  | 1.05 us: 1.02x slower                                                    |
| sqlglot_v2_normalize             | 44.5 ms                                                                  | 45.2 ms: 1.02x slower                                                    |
| bench_mp_pool                    | 43.1 ms                                                                  | 43.8 ms: 1.02x slower                                                    |
| raytrace                         | 113 ms                                                                   | 115 ms: 1.02x slower                                                     |
| sqlglot_v2_optimize              | 21.5 ms                                                                  | 21.9 ms: 1.02x slower                                                    |
| genshi_xml                       | 20.4 ms                                                                  | 20.8 ms: 1.02x slower                                                    |
| logging_format                   | 2.34 us                                                                  | 2.38 us: 1.02x slower                                                    |
| thrift                           | 296 us                                                                   | 301 us: 1.02x slower                                                     |
| dulwich_log                      | 17.8 ms                                                                  | 18.1 ms: 1.02x slower                                                    |
| deepcopy                         | 94.4 us                                                                  | 96.2 us: 1.02x slower                                                    |
| async_tree_none_tg               | 94.0 ms                                                                  | 95.8 ms: 1.02x slower                                                    |
| logging_simple                   | 2.12 us                                                                  | 2.16 us: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 116 ms                                                                   | 118 ms: 1.02x slower                                                     |
| xml_etree_iterparse              | 39.0 ms                                                                  | 39.8 ms: 1.02x slower                                                    |
| docutils                         | 972 ms                                                                   | 991 ms: 1.02x slower                                                     |
| asyncio_websockets               | 181 ms                                                                   | 184 ms: 1.02x slower                                                     |
| json_dumps                       | 3.77 ms                                                                  | 3.84 ms: 1.02x slower                                                    |
| deltablue                        | 1.40 ms                                                                  | 1.43 ms: 1.02x slower                                                    |
| mdp                              | 527 ms                                                                   | 538 ms: 1.02x slower                                                     |
| deepcopy_memo                    | 11.0 us                                                                  | 11.2 us: 1.02x slower                                                    |
| async_tree_eager                 | 38.8 ms                                                                  | 39.6 ms: 1.02x slower                                                    |
| crypto_pyaes                     | 36.5 ms                                                                  | 37.3 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.3 ms                                                                  | 48.3 ms: 1.02x slower                                                    |
| genshi_text                      | 9.43 ms                                                                  | 9.65 ms: 1.02x slower                                                    |
| logging_silent                   | 39.7 ns                                                                  | 40.7 ns: 1.02x slower                                                    |
| async_tree_none                  | 98.6 ms                                                                  | 101 ms: 1.02x slower                                                     |
| django_template                  | 14.2 ms                                                                  | 14.6 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 60.8 us                                                                  | 62.3 us: 1.02x slower                                                    |
| async_tree_cpu_io_mixed          | 246 ms                                                                   | 253 ms: 1.03x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 226 ms                                                                   | 232 ms: 1.03x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 211 ms                                                                   | 216 ms: 1.03x slower                                                     |
| comprehensions                   | 6.86 us                                                                  | 7.03 us: 1.03x slower                                                    |
| async_tree_eager_tg              | 76.8 ms                                                                  | 78.8 ms: 1.03x slower                                                    |
| async_tree_memoization_tg        | 131 ms                                                                   | 135 ms: 1.03x slower                                                     |
| async_tree_cpu_io_mixed_tg       | 240 ms                                                                   | 247 ms: 1.03x slower                                                     |
| subparsers                       | 3.83 ms                                                                  | 3.94 ms: 1.03x slower                                                    |
| chaos                            | 24.9 ms                                                                  | 25.7 ms: 1.03x slower                                                    |
| bpe_tokeniser                    | 1.91 sec                                                                 | 1.97 sec: 1.03x slower                                                   |
| scimark_fft                      | 117 ms                                                                   | 120 ms: 1.03x slower                                                     |
| async_tree_io                    | 219 ms                                                                   | 226 ms: 1.03x slower                                                     |
| hexiom                           | 2.65 ms                                                                  | 2.73 ms: 1.03x slower                                                    |
| async_tree_eager_io              | 212 ms                                                                   | 219 ms: 1.03x slower                                                     |
| many_optionals                   | 236 us                                                                   | 244 us: 1.03x slower                                                     |
| async_tree_io_tg                 | 219 ms                                                                   | 226 ms: 1.03x slower                                                     |
| 2to3                             | 107 ms                                                                   | 111 ms: 1.04x slower                                                     |
| async_generators                 | 168 ms                                                                   | 175 ms: 1.04x slower                                                     |
| async_tree_eager_io_tg           | 211 ms                                                                   | 221 ms: 1.05x slower                                                     |
| xml_etree_parse                  | 60.3 ms                                                                  | 63.4 ms: 1.05x slower                                                    |
| scimark_lu                       | 43.0 ms                                                                  | 45.9 ms: 1.07x slower                                                    |
| Geometric mean                   | (ref)                                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (20): sqlite_synth, regex_effbot, python_startup, unpickle_pure_python, nqueens, python_startup_no_site, dask, coroutines, k_core, xml_etree_generate, richards_super, pickle_pure_python, json_loads, tomli_loads, pprint_safe_repr, sympy_sum, create_gc_cycles, regex_dna, pycparser, pylint
Ignored benchmarks (8) of results/bm-20260130-3.15.0a5+-ccbe41e/bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.014x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.00x