# Results vs. 3.13.0rc2

- fork: python
- ref: d19de375a204c74ab5f3
- machine: darwin-arm64
- commit hash: d19de37
- commit date: 2026-03-11
- overall geometric mean: 1.084x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| docutils       | 1.05 sec                                                       | 994 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 21.0 ms: 1.10x faster                                                    |
| sphinx         | 409 ms                                                         | 390 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 223 ms: 2.36x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 224 ms: 1.81x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 233 ms: 1.66x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.8 ms: 1.43x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.35x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.5 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.2 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.3 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.8 ms: 1.17x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.8 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.91 ms: 1.08x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.52 ms: 1.06x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.8 ms: 1.05x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.0 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 816 ms: 1.22x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 97.5 us: 1.02x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 62.1 ms: 1.01x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.83 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.38 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.78 ms: 1.02x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| mako            | 4.41 ms                                                        | 4.76 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 14.5 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 223 ms: 2.36x faster                                                     |
| mdp                              | 1.06 sec                                                       | 532 ms: 1.99x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 224 ms: 1.81x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 233 ms: 1.66x faster                                                     |
| k_core                           | 1.46 sec                                                       | 897 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.98 ms: 1.57x faster                                                    |
| deepcopy                         | 145 us                                                         | 97.7 us: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.8 ms: 1.43x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                    |
| go                               | 72.6 ms                                                        | 52.5 ms: 1.38x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.35x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.5 ms: 1.35x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.9 ms: 1.28x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 816 ms: 1.22x faster                                                     |
| pyflate                          | 222 ms                                                         | 182 ms: 1.22x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| float                            | 31.4 ms                                                        | 26.8 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| richards                         | 22.1 ms                                                        | 19.8 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 898 us: 1.11x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 22.4 ms: 1.10x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.0 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.82 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.91 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.2 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.8 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| fannkuch                         | 179 ms                                                         | 167 ms: 1.07x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.06x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.52 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 994 ms: 1.05x faster                                                     |
| sphinx                           | 409 ms                                                         | 390 ms: 1.05x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.72 ms: 1.05x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.13 us: 1.05x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.34 us: 1.05x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 35.6 ms: 1.05x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 45.8 ms: 1.05x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 42.2 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 630 ms: 1.03x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 312 ms: 1.03x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| pycparser                        | 470 ms                                                         | 460 ms: 1.02x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 63.2 us: 1.02x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.78 ms: 1.02x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 97.5 us: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.38 ms: 1.02x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 122 ms: 1.01x faster                                                     |
| logging_silent                   | 40.6 ns                                                        | 40.2 ns: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 306 us: 1.01x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.03 ms: 1.01x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 62.1 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| meteor_contest                   | 47.9 ms                                                        | 48.9 ms: 1.02x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.83 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 97.0 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.83 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.3 ms: 1.03x slower                                                    |
| raytrace                         | 109 ms                                                         | 113 ms: 1.03x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.07 us: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 44.5 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.9 ms: 1.05x slower                                                    |
| nbody                            | 42.5 ms                                                        | 44.8 ms: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.4 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.38 ms: 1.07x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.76 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.6 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.15x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.5 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.7 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.3 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 251 us: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.3 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (5): json_loads, sqlite_synth, chaos, connected_components, deltablue
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260311-3.15.0a7+-d19de37/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.084x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.19x