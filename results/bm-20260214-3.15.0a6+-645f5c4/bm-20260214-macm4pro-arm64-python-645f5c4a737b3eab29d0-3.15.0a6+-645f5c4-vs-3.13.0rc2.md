# Results vs. 3.13.0rc2

- fork: python
- ref: 645f5c4a737b3eab29d0
- machine: darwin-arm64
- commit hash: 645f5c4
- commit date: 2026-02-14
- overall geometric mean: 1.082x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.3 ms: 1.09x faster                                                    |
| sphinx         | 409 ms                                                         | 389 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.40x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 223 ms: 2.34x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 225 ms: 1.71x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 97.0 ms: 1.37x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 250 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 257 ms: 1.14x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.1 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.7 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 43.9 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.12x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.53 ms: 1.12x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 44.9 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.75 ms: 1.24x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 830 ms: 1.20x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 94.8 us: 1.05x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.7 ms: 1.02x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 138 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.73 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.31 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.56 ms: 1.04x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.8 ms: 1.03x faster                                                    |
| mako            | 4.41 ms                                                        | 4.65 ms: 1.05x slower                                                    |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.40x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 223 ms: 2.34x faster                                                     |
| mdp                              | 1.06 sec                                                       | 533 ms: 1.98x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 225 ms: 1.71x faster                                                     |
| k_core                           | 1.46 sec                                                       | 897 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.01 ms: 1.56x faster                                                    |
| deepcopy                         | 145 us                                                         | 96.6 us: 1.50x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.44x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.38x faster                                                     |
| go                               | 72.6 ms                                                        | 52.5 ms: 1.38x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 97.0 ms: 1.37x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.35x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.0 ms: 1.28x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.75 ms: 1.24x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.23x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 830 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 250 ms: 1.20x faster                                                     |
| pyflate                          | 222 ms                                                         | 189 ms: 1.17x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 257 ms: 1.14x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| richards                         | 22.1 ms                                                        | 19.6 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.53 ms: 1.12x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.1 ms: 1.12x faster                                                    |
| float                            | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 910 us: 1.09x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.82 ms: 1.09x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.3 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.1 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.9 ms: 1.07x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 44.9 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                    |
| fannkuch                         | 179 ms                                                         | 168 ms: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| sphinx                           | 409 ms                                                         | 389 ms: 1.05x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 94.8 us: 1.05x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.56 ms: 1.04x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 308 ms: 1.04x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.73 ms: 1.04x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 627 ms: 1.04x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                                     |
| pycparser                        | 470 ms                                                         | 458 ms: 1.03x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 20.8 ms: 1.03x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.1 us: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.42 ms: 1.01x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.41 us: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 938 ns: 1.01x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| deltablue                        | 1.45 ms                                                        | 1.44 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 208 ms: 1.00x faster                                                     |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.73 ms: 1.01x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.7 ms: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.8 ms: 1.02x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.99 us: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.3 ms: 1.03x slower                                                    |
| nbody                            | 42.5 ms                                                        | 43.9 ms: 1.03x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.8 ms: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 431 us: 1.05x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 54.9 ms: 1.05x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.65 ms: 1.05x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 46.1 ms: 1.06x slower                                                    |
| raytrace                         | 109 ms                                                         | 115 ms: 1.06x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.31 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 138 us: 1.06x slower                                                     |
| chaos                            | 24.3 ms                                                        | 25.9 ms: 1.07x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 45.7 ms: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.91 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.08x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.8 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.0 ms: 1.19x slower                                                    |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.7 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (4): gc_traversal, regex_dna, thrift, logging_silent
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260214-3.15.0a6+-645f5c4/bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.18x