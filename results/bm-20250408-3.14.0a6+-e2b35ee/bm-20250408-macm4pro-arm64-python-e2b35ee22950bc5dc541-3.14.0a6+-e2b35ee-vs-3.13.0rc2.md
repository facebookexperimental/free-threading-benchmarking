# Results vs. 3.13.0rc2

- fork: python
- ref: e2b35ee22950bc5dc541
- machine: darwin-arm64
- commit hash: e2b35ee
- commit date: 2025-04-08
- overall geometric mean: 1.025x faster
- HPT reliability: 67.73%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.02x faster                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.12x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.55x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 170 ms: 1.14x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 42.9 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.4 ms: 3.09x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                    |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 49.8 ms: 1.17x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                    |
| regex_dna      | 94.6 ms                                                        | 97.2 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 917 ms: 1.09x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.8 ms: 1.03x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.9 ms: 1.02x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.7 ms: 1.03x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 103 us: 1.03x slower                                                     |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 4.90 ms: 1.05x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.96 ms: 1.04x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.74 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.02x slower                                                    |
| mako            | 4.41 ms                                                        | 4.84 ms: 1.10x slower                                                    |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.12x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                     |
| mdp                              | 1.06 sec                                                       | 525 ms: 2.01x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                     |
| k_core                           | 1.46 sec                                                       | 946 ms: 1.55x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.55x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                    |
| deepcopy                         | 145 us                                                         | 110 us: 1.31x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                     |
| go                               | 72.6 ms                                                        | 57.8 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 51.1 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 867 us: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 170 ms: 1.14x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 196 ms: 1.14x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 17.6 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 917 ms: 1.09x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                     |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| connected_components             | 208 ms                                                         | 201 ms: 1.03x faster                                                     |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.8 ms: 1.03x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 1.99 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| 2to3                             | 112 ms                                                         | 110 ms: 1.02x faster                                                     |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 936 ns: 1.01x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.03 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.46 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.01x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.9 ms: 1.01x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.8 ms: 1.00x faster                                                    |
| coverage                         | 31.2 ms                                                        | 31.5 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 65.2 us: 1.01x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 45.0 ms: 1.01x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.2 ns: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                                     |
| fannkuch                         | 179 ms                                                         | 182 ms: 1.02x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 663 ms: 1.02x slower                                                     |
| richards                         | 22.1 ms                                                        | 22.5 ms: 1.02x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.9 ms: 1.02x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.7 ms: 1.03x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.2 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 103 us: 1.03x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.96 ms: 1.04x slower                                                    |
| pycparser                        | 470 ms                                                         | 490 ms: 1.04x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 100.0 ms: 1.05x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 433 us: 1.05x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 39.8 ms: 1.05x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.90 ms: 1.05x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.0 ms: 1.05x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.3 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.54 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.0 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                     |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.37 ms: 1.07x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.42 us: 1.08x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.65 us: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.84 ms: 1.10x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 48.2 ms: 1.10x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.96 ms: 1.10x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.9 ms: 1.11x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.6 ms: 1.11x slower                                                    |
| raytrace                         | 109 ms                                                         | 121 ms: 1.11x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.12x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.66 us: 1.13x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.74 ms: 1.13x slower                                                    |
| many_optionals                   | 200 us                                                         | 229 us: 1.14x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.1 ms: 1.15x slower                                                    |
| nbody                            | 42.5 ms                                                        | 49.8 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.64 ms: 1.38x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.4 ms: 3.09x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (3): coroutines, hexiom, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250408-3.14.0a6+-e2b35ee/bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.025x faster

# HPT report

- Reliability score: 67.73% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.08x