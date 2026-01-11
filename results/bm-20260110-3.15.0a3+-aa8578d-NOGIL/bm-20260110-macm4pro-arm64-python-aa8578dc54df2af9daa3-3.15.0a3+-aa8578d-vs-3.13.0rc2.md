# Results vs. 3.13.0rc2

- fork: python
- ref: aa8578dc54df2af9daa3
- machine: darwin-arm64
- commit hash: aa8578d
- commit date: 2026-01-10
- overall geometric mean: 1.015x faster
- HPT reliability: 50.15%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| sphinx         | 409 ms                                                         | 423 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 242 ms: 2.15x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.12x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 238 ms: 1.70x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.55x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 152 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.3 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.9 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                             |

Benchmark hidden because not significant (2): coroutines, async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.1 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.27 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.8 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.7 ms: 1.22x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.96 ms: 1.17x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 897 ms: 1.11x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 56.2 ms: 1.11x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.08x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.69 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.04 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.4 ms: 1.09x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| mako            | 4.41 ms                                                        | 5.50 ms: 1.25x slower                                                    |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.18x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 801 us: 2.55x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 242 ms: 2.15x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.12x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 506 us: 1.96x faster                                                     |
| mdp                              | 1.06 sec                                                       | 603 ms: 1.76x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 238 ms: 1.70x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.55x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.16 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 991 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 106 us: 1.37x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.23x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.7 ms: 1.22x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 152 ms: 1.22x faster                                                     |
| go                               | 72.6 ms                                                        | 60.0 ms: 1.21x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.3 ms: 1.18x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.96 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.27 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 194 ms: 1.15x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 829 ns: 1.14x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 897 ms: 1.11x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 56.2 ms: 1.11x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| float                            | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                     |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 124 ms: 1.01x slower                                                     |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 332 ms: 1.03x slower                                                     |
| sphinx                           | 409 ms                                                         | 423 ms: 1.04x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.0 ms: 1.04x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 680 ms: 1.05x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.8 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.02 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.3 ms: 1.07x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.4 ns: 1.07x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.42 us: 1.08x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.08x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.5 ms: 1.09x slower                                                    |
| thrift                           | 309 us                                                         | 337 us: 1.09x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 23.4 ms: 1.09x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 70.7 us: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.3 ms: 1.09x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.68 us: 1.10x slower                                                    |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                    |
| shortest_path                    | 225 ms                                                         | 251 ms: 1.12x slower                                                     |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.69 ms: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.13x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 42.8 ms: 1.15x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.4 ms: 1.15x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.4 ms: 1.15x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.2 ms: 1.16x slower                                                    |
| raytrace                         | 109 ms                                                         | 127 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.8 ms: 1.16x slower                                                    |
| connected_components             | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.10 ms: 1.18x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.04 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.29 us: 1.22x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.3 ms: 1.22x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.9 ms: 1.25x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.50 ms: 1.25x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 41.9 ms: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| generators                       | 15.7 ms                                                        | 20.8 ms: 1.32x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 549 us: 1.33x slower                                                     |
| nbody                            | 42.5 ms                                                        | 57.1 ms: 1.34x slower                                                    |
| many_optionals                   | 200 us                                                         | 271 us: 1.35x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 59.8 ms: 1.40x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.9 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (6): pycparser, coroutines, json, regex_dna, async_tree_eager_cpu_io_mixed, html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260110-3.15.0a3+-aa8578d-NOGIL/bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.015x faster

# HPT report

- Reliability score: 50.15% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x