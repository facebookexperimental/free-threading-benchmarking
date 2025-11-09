# Results vs. 3.13.0rc2

- fork: python
- ref: 0ac890bea79d3e0162c8
- machine: darwin-arm64
- commit hash: 0ac890b
- commit date: 2025-11-08
- overall geometric mean: 1.045x faster
- HPT reliability: 99.60%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                    |
| sphinx         | 409 ms                                                         | 395 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.32x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 224 ms: 1.81x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 228 ms: 1.69x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.34x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.0 ms: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 248 ms: 1.19x faster                                                     |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.9 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 236 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 125 ms: 1.22x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.3 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 48.9 ms: 1.15x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.84 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.5 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 48.2 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.85 ms: 1.21x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.6 ms: 1.19x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 893 ms: 1.12x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 60.7 ms: 1.03x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 98.5 us: 1.01x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.5 ms: 1.01x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 144 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.75 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                    |
| mako            | 4.41 ms                                                        | 4.83 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.32x faster                                                     |
| mdp                              | 1.06 sec                                                       | 533 ms: 1.99x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 224 ms: 1.81x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 228 ms: 1.69x faster                                                     |
| k_core                           | 1.46 sec                                                       | 896 ms: 1.63x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.0 us: 1.37x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.34x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.0 ms: 1.34x faster                                                    |
| go                               | 72.6 ms                                                        | 54.6 ms: 1.33x faster                                                    |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.31x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.9 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.85 ms: 1.21x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.6 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 248 ms: 1.19x faster                                                     |
| pyflate                          | 222 ms                                                         | 189 ms: 1.18x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                     |
| float                            | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 893 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 899 us: 1.10x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.84 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.89 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.9 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.5 ms: 1.05x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.7 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| sphinx                           | 409 ms                                                         | 395 ms: 1.03x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.9 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.7 ms: 1.03x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.80 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 205 ms: 1.01x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 93.5 ms: 1.01x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.02 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.5 us: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 466 ms: 1.01x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.5 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.49 ms: 1.00x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.44 ms: 1.00x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 48.2 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.80 ms: 1.01x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 416 us: 1.01x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.75 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 65.7 us: 1.02x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.49 us: 1.02x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.28 us: 1.02x slower                                                    |
| thrift                           | 309 us                                                         | 316 us: 1.02x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 664 ms: 1.02x slower                                                     |
| sqlite_synth                     | 948 ns                                                         | 971 ns: 1.02x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 332 ms: 1.03x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.3 ms: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.2 ms: 1.05x slower                                                    |
| raytrace                         | 109 ms                                                         | 115 ms: 1.06x slower                                                     |
| chaos                            | 24.3 ms                                                        | 25.8 ms: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 103 ms: 1.08x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.4 ms: 1.08x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.36 us: 1.08x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 36.5 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.83 ms: 1.09x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 175 ms: 1.10x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 41.5 ms: 1.10x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.10x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 48.3 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 236 ms: 1.13x slower                                                     |
| generators                       | 15.7 ms                                                        | 17.8 ms: 1.14x slower                                                    |
| nbody                            | 42.5 ms                                                        | 48.9 ms: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 125 ms: 1.22x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| many_optionals                   | 200 us                                                         | 351 us: 1.75x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 17.5 ms: 2.80x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.3 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (6): json_loads, fannkuch, 2to3, scimark_fft, spectral_norm, logging_silent
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251108-3.15.0a1+-0ac890b/bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.045x faster

# HPT report

- Reliability score: 99.60% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.16x