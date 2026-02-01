# Results vs. default_base_vs_NOGIL

- fork: python
- ref: ccbe41e27cdb44103318
- machine: darwin-arm64
- commit hash: ccbe41e
- commit date: 2026-01-30
- overall geometric mean: 1.068x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 107 ms                                                                   | 119 ms: 1.11x slower                                                     |
| docutils       | 972 ms                                                                   | 980 ms: 1.01x slower                                                     |
| html5lib       | 20.7 ms                                                                  | 22.4 ms: 1.08x slower                                                    |
| sphinx         | 377 ms                                                                   | 405 ms: 1.07x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.07x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines                       | 10.1 ms                                                                  | 10.2 ms: 1.01x slower                                                    |
| asyncio_websockets               | 181 ms                                                                   | 186 ms: 1.03x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 211 ms                                                                   | 219 ms: 1.04x slower                                                     |
| async_tree_cpu_io_mixed_tg       | 240 ms                                                                   | 252 ms: 1.05x slower                                                     |
| async_tree_cpu_io_mixed          | 246 ms                                                                   | 260 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 226 ms                                                                   | 241 ms: 1.06x slower                                                     |
| async_tree_eager_memoization     | 104 ms                                                                   | 111 ms: 1.07x slower                                                     |
| async_generators                 | 168 ms                                                                   | 181 ms: 1.08x slower                                                     |
| async_tree_memoization_tg        | 131 ms                                                                   | 142 ms: 1.08x slower                                                     |
| async_tree_eager_memoization_tg  | 116 ms                                                                   | 127 ms: 1.10x slower                                                     |
| async_tree_io                    | 219 ms                                                                   | 242 ms: 1.11x slower                                                     |
| async_tree_memoization           | 134 ms                                                                   | 149 ms: 1.11x slower                                                     |
| async_tree_io_tg                 | 219 ms                                                                   | 243 ms: 1.11x slower                                                     |
| async_tree_none                  | 98.6 ms                                                                  | 112 ms: 1.13x slower                                                     |
| async_tree_eager_io_tg           | 211 ms                                                                   | 239 ms: 1.14x slower                                                     |
| async_tree_eager_io              | 212 ms                                                                   | 242 ms: 1.14x slower                                                     |
| async_tree_none_tg               | 94.0 ms                                                                  | 108 ms: 1.15x slower                                                     |
| async_tree_eager                 | 38.8 ms                                                                  | 45.9 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 76.8 ms                                                                  | 91.4 ms: 1.19x slower                                                    |
| Geometric mean                   | (ref)                                                                    | 1.10x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 156 ms                                                                   | 157 ms: 1.01x slower                                                     |
| float          | 27.6 ms                                                                  | 28.4 ms: 1.03x slower                                                    |
| nbody          | 43.8 ms                                                                  | 58.0 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.11x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 9.39 ms                                                                  | 8.97 ms: 1.05x faster                                                    |
| regex_dna      | 92.1 ms                                                                  | 91.4 ms: 1.01x faster                                                    |
| regex_effbot   | 1.43 ms                                                                  | 1.42 ms: 1.01x faster                                                    |
| regex_compile  | 44.1 ms                                                                  | 49.5 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 60.3 ms                                                                  | 57.3 ms: 1.05x faster                                                    |
| xml_etree_iterparse  | 39.0 ms                                                                  | 38.8 ms: 1.01x faster                                                    |
| json_dumps           | 3.77 ms                                                                  | 3.89 ms: 1.03x slower                                                    |
| pickle_pure_python   | 136 us                                                                   | 142 us: 1.05x slower                                                     |
| tomli_loads          | 814 ms                                                                   | 866 ms: 1.06x slower                                                     |
| json_loads           | 10.4 us                                                                  | 11.1 us: 1.06x slower                                                    |
| xml_etree_generate   | 33.9 ms                                                                  | 36.5 ms: 1.08x slower                                                    |
| xml_etree_process    | 23.9 ms                                                                  | 26.4 ms: 1.10x slower                                                    |
| unpickle_pure_python | 95.6 us                                                                  | 106 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                                    | 1.05x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.65 ms                                                                  | 9.61 ms: 1.11x slower                                                    |
| python_startup_no_site | 6.23 ms                                                                  | 7.00 ms: 1.12x slower                                                    |
| Geometric mean         | (ref)                                                                    | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|-----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 20.4 ms                                                                  | 21.7 ms: 1.06x slower                                                    |
| django_template | 14.2 ms                                                                  | 15.3 ms: 1.08x slower                                                    |
| genshi_text     | 9.43 ms                                                                  | 10.6 ms: 1.13x slower                                                    |
| mako            | 4.61 ms                                                                  | 5.42 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                                    | 1.11x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 1.97 ms                                                                  | 766 us: 2.56x faster                                                     |
| create_gc_cycles                 | 875 us                                                                   | 496 us: 1.76x faster                                                     |
| sqlite_synth                     | 951 ns                                                                   | 810 ns: 1.17x faster                                                     |
| xml_etree_parse                  | 60.3 ms                                                                  | 57.3 ms: 1.05x faster                                                    |
| regex_v8                         | 9.39 ms                                                                  | 8.97 ms: 1.05x faster                                                    |
| regex_dna                        | 92.1 ms                                                                  | 91.4 ms: 1.01x faster                                                    |
| regex_effbot                     | 1.43 ms                                                                  | 1.42 ms: 1.01x faster                                                    |
| xml_etree_iterparse              | 39.0 ms                                                                  | 38.8 ms: 1.01x faster                                                    |
| docutils                         | 972 ms                                                                   | 980 ms: 1.01x slower                                                     |
| pidigits                         | 156 ms                                                                   | 157 ms: 1.01x slower                                                     |
| dulwich_log                      | 17.8 ms                                                                  | 18.0 ms: 1.01x slower                                                    |
| dask                             | 521 ms                                                                   | 527 ms: 1.01x slower                                                     |
| coroutines                       | 10.1 ms                                                                  | 10.2 ms: 1.01x slower                                                    |
| fannkuch                         | 166 ms                                                                   | 170 ms: 1.03x slower                                                     |
| bpe_tokeniser                    | 1.91 sec                                                                 | 1.96 sec: 1.03x slower                                                   |
| float                            | 27.6 ms                                                                  | 28.4 ms: 1.03x slower                                                    |
| asyncio_websockets               | 181 ms                                                                   | 186 ms: 1.03x slower                                                     |
| json_dumps                       | 3.77 ms                                                                  | 3.89 ms: 1.03x slower                                                    |
| json                             | 1.84 ms                                                                  | 1.90 ms: 1.03x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 211 ms                                                                   | 219 ms: 1.04x slower                                                     |
| pyflate                          | 185 ms                                                                   | 193 ms: 1.04x slower                                                     |
| pylint                           | 110 ms                                                                   | 115 ms: 1.04x slower                                                     |
| async_tree_cpu_io_mixed_tg       | 240 ms                                                                   | 252 ms: 1.05x slower                                                     |
| pickle_pure_python               | 136 us                                                                   | 142 us: 1.05x slower                                                     |
| bench_mp_pool                    | 43.1 ms                                                                  | 45.2 ms: 1.05x slower                                                    |
| async_tree_cpu_io_mixed          | 246 ms                                                                   | 260 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 226 ms                                                                   | 241 ms: 1.06x slower                                                     |
| genshi_xml                       | 20.4 ms                                                                  | 21.7 ms: 1.06x slower                                                    |
| tomli_loads                      | 814 ms                                                                   | 866 ms: 1.06x slower                                                     |
| json_loads                       | 10.4 us                                                                  | 11.1 us: 1.06x slower                                                    |
| sqlglot_v2_normalize             | 44.5 ms                                                                  | 47.4 ms: 1.07x slower                                                    |
| subparsers                       | 3.83 ms                                                                  | 4.08 ms: 1.07x slower                                                    |
| async_tree_eager_memoization     | 104 ms                                                                   | 111 ms: 1.07x slower                                                     |
| telco                            | 2.81 ms                                                                  | 3.01 ms: 1.07x slower                                                    |
| sphinx                           | 377 ms                                                                   | 405 ms: 1.07x slower                                                     |
| xml_etree_generate               | 33.9 ms                                                                  | 36.5 ms: 1.08x slower                                                    |
| django_template                  | 14.2 ms                                                                  | 15.3 ms: 1.08x slower                                                    |
| async_generators                 | 168 ms                                                                   | 181 ms: 1.08x slower                                                     |
| async_tree_memoization_tg        | 131 ms                                                                   | 142 ms: 1.08x slower                                                     |
| html5lib                         | 20.7 ms                                                                  | 22.4 ms: 1.08x slower                                                    |
| sqlglot_v2_optimize              | 21.5 ms                                                                  | 23.4 ms: 1.09x slower                                                    |
| pprint_safe_repr                 | 301 ms                                                                   | 329 ms: 1.09x slower                                                     |
| sympy_integrate                  | 7.22 ms                                                                  | 7.90 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 116 ms                                                                   | 127 ms: 1.10x slower                                                     |
| scimark_fft                      | 117 ms                                                                   | 128 ms: 1.10x slower                                                     |
| deepcopy_reduce                  | 1.04 us                                                                  | 1.14 us: 1.10x slower                                                    |
| chaos                            | 24.9 ms                                                                  | 27.4 ms: 1.10x slower                                                    |
| thrift                           | 296 us                                                                   | 326 us: 1.10x slower                                                     |
| pprint_pformat                   | 610 ms                                                                   | 673 ms: 1.10x slower                                                     |
| xml_etree_process                | 23.9 ms                                                                  | 26.4 ms: 1.10x slower                                                    |
| many_optionals                   | 236 us                                                                   | 260 us: 1.10x slower                                                     |
| logging_silent                   | 39.7 ns                                                                  | 43.8 ns: 1.10x slower                                                    |
| unpickle_pure_python             | 95.6 us                                                                  | 106 us: 1.10x slower                                                     |
| sympy_str                        | 97.6 ms                                                                  | 108 ms: 1.10x slower                                                     |
| k_core                           | 895 ms                                                                   | 988 ms: 1.10x slower                                                     |
| async_tree_io                    | 219 ms                                                                   | 242 ms: 1.11x slower                                                     |
| async_tree_memoization           | 134 ms                                                                   | 149 ms: 1.11x slower                                                     |
| sympy_expand                     | 165 ms                                                                   | 183 ms: 1.11x slower                                                     |
| sympy_sum                        | 53.6 ms                                                                  | 59.5 ms: 1.11x slower                                                    |
| sqlglot_v2_transpile             | 611 us                                                                   | 677 us: 1.11x slower                                                     |
| python_startup                   | 8.65 ms                                                                  | 9.61 ms: 1.11x slower                                                    |
| 2to3                             | 107 ms                                                                   | 119 ms: 1.11x slower                                                     |
| scimark_sor                      | 48.8 ms                                                                  | 54.2 ms: 1.11x slower                                                    |
| deepcopy                         | 94.4 us                                                                  | 105 us: 1.11x slower                                                     |
| async_tree_io_tg                 | 219 ms                                                                   | 243 ms: 1.11x slower                                                     |
| raytrace                         | 113 ms                                                                   | 126 ms: 1.11x slower                                                     |
| deepcopy_memo                    | 11.0 us                                                                  | 12.3 us: 1.12x slower                                                    |
| scimark_sparse_mat_mult          | 1.88 ms                                                                  | 2.11 ms: 1.12x slower                                                    |
| logging_format                   | 2.34 us                                                                  | 2.62 us: 1.12x slower                                                    |
| logging_simple                   | 2.12 us                                                                  | 2.38 us: 1.12x slower                                                    |
| regex_compile                    | 44.1 ms                                                                  | 49.5 ms: 1.12x slower                                                    |
| deltablue                        | 1.40 ms                                                                  | 1.58 ms: 1.12x slower                                                    |
| python_startup_no_site           | 6.23 ms                                                                  | 7.00 ms: 1.12x slower                                                    |
| spectral_norm                    | 44.5 ms                                                                  | 50.0 ms: 1.12x slower                                                    |
| sqlglot_v2_parse                 | 497 us                                                                   | 559 us: 1.12x slower                                                     |
| genshi_text                      | 9.43 ms                                                                  | 10.6 ms: 1.13x slower                                                    |
| async_tree_none                  | 98.6 ms                                                                  | 112 ms: 1.13x slower                                                     |
| mdp                              | 527 ms                                                                   | 598 ms: 1.13x slower                                                     |
| async_tree_eager_io_tg           | 211 ms                                                                   | 239 ms: 1.14x slower                                                     |
| shortest_path                    | 222 ms                                                                   | 253 ms: 1.14x slower                                                     |
| nqueens                          | 36.9 ms                                                                  | 41.9 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.3 ms                                                                  | 54.0 ms: 1.14x slower                                                    |
| async_tree_eager_io              | 212 ms                                                                   | 242 ms: 1.14x slower                                                     |
| crypto_pyaes                     | 36.5 ms                                                                  | 41.8 ms: 1.14x slower                                                    |
| async_tree_none_tg               | 94.0 ms                                                                  | 108 ms: 1.15x slower                                                     |
| richards                         | 19.4 ms                                                                  | 22.4 ms: 1.16x slower                                                    |
| go                               | 50.9 ms                                                                  | 58.8 ms: 1.16x slower                                                    |
| typing_runtime_protocols         | 60.8 us                                                                  | 70.5 us: 1.16x slower                                                    |
| generators                       | 17.8 ms                                                                  | 20.6 ms: 1.16x slower                                                    |
| richards_super                   | 21.9 ms                                                                  | 25.6 ms: 1.17x slower                                                    |
| hexiom                           | 2.65 ms                                                                  | 3.10 ms: 1.17x slower                                                    |
| scimark_monte_carlo              | 27.4 ms                                                                  | 32.2 ms: 1.18x slower                                                    |
| mako                             | 4.61 ms                                                                  | 5.42 ms: 1.18x slower                                                    |
| async_tree_eager                 | 38.8 ms                                                                  | 45.9 ms: 1.18x slower                                                    |
| comprehensions                   | 6.86 us                                                                  | 8.11 us: 1.18x slower                                                    |
| async_tree_eager_tg              | 76.8 ms                                                                  | 91.4 ms: 1.19x slower                                                    |
| connected_components             | 204 ms                                                                   | 246 ms: 1.20x slower                                                     |
| coverage                         | 30.7 ms                                                                  | 38.4 ms: 1.25x slower                                                    |
| bench_thread_pool                | 430 us                                                                   | 562 us: 1.31x slower                                                     |
| nbody                            | 43.8 ms                                                                  | 58.0 ms: 1.33x slower                                                    |
| scimark_lu                       | 43.0 ms                                                                  | 57.3 ms: 1.33x slower                                                    |
| Geometric mean                   | (ref)                                                                    | 1.08x slower                                                             |

Benchmark hidden because not significant (2): pathlib, pycparser
Ignored benchmarks (8) of results/bm-20260130-3.15.0a5+-ccbe41e-NOGIL/bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.068x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.11x