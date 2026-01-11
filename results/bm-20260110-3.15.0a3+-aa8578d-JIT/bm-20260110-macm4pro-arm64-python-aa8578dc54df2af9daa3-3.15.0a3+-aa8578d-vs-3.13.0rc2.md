# Results vs. 3.13.0rc2

- fork: python
- ref: aa8578dc54df2af9daa3
- machine: darwin-arm64
- commit hash: aa8578d
- commit date: 2026-01-10
- overall geometric mean: 1.151x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.02x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 20.0 ms: 1.16x faster                                                    |
| sphinx         | 409 ms                                                         | 390 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 222 ms: 2.37x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.36x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 221 ms: 1.83x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 229 ms: 1.68x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 97.5 ms: 1.46x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 96.8 ms: 1.37x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 248 ms: 1.19x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 37.0 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.1 ms: 2.70x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 22.7 ms: 1.38x faster                                                    |
| nbody          | 42.5 ms                                                        | 40.0 ms: 1.06x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                          | 1.14x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 40.5 ms: 1.18x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.6 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 693 ms: 1.44x faster                                                     |
| unpickle_pure_python | 99.5 us                                                        | 73.7 us: 1.35x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.60 ms: 1.29x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 36.8 ms: 1.25x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 112 us: 1.16x faster                                                     |
| xml_etree_process    | 25.4 ms                                                        | 21.8 ms: 1.16x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 30.9 ms: 1.16x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.2 ms: 1.04x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| Geometric mean       | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.90 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.41 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 3.91 ms: 1.13x faster                                                    |
| genshi_text     | 9.97 ms                                                        | 8.94 ms: 1.12x faster                                                    |
| django_template | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 222 ms: 2.37x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.36x faster                                                     |
| richards                         | 22.1 ms                                                        | 9.76 ms: 2.26x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 11.6 ms: 2.13x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 221 ms: 1.83x faster                                                     |
| mdp                              | 1.06 sec                                                       | 591 ms: 1.79x faster                                                     |
| go                               | 72.6 ms                                                        | 42.6 ms: 1.70x faster                                                    |
| k_core                           | 1.46 sec                                                       | 864 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 229 ms: 1.68x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.96 ms: 1.58x faster                                                    |
| deepcopy                         | 145 us                                                         | 93.5 us: 1.55x faster                                                    |
| pyflate                          | 222 ms                                                         | 144 ms: 1.54x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 42.5 ms: 1.51x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 97.5 ms: 1.46x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 693 ms: 1.44x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.44x faster                                                    |
| float                            | 31.4 ms                                                        | 22.7 ms: 1.38x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 96.8 ms: 1.37x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 21.8 ms: 1.37x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 953 ns: 1.36x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.35x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 73.7 us: 1.35x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.60 ms: 1.29x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.13 ms: 1.29x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 254 ms: 1.27x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 518 ms: 1.25x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.8 ms: 1.25x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 100 ms: 1.23x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.55 ms: 1.20x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 33.8 ns: 1.20x faster                                                    |
| scimark_lu                       | 42.8 ms                                                        | 35.7 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 248 ms: 1.19x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 40.5 ms: 1.18x faster                                                    |
| fannkuch                         | 179 ms                                                         | 152 ms: 1.18x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 37.0 ms: 1.17x faster                                                    |
| pickle_pure_python               | 130 us                                                         | 112 us: 1.16x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 21.8 ms: 1.16x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 30.9 ms: 1.16x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 20.0 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.85 sec: 1.15x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| mako                             | 4.41 ms                                                        | 3.91 ms: 1.13x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 8.94 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                    |
| chaos                            | 24.3 ms                                                        | 22.0 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| comprehensions                   | 6.80 us                                                        | 6.21 us: 1.09x faster                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 30.9 ms: 1.09x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 40.4 ms: 1.08x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.65 ms: 1.07x faster                                                    |
| nbody                            | 42.5 ms                                                        | 40.0 ms: 1.06x faster                                                    |
| json                             | 1.94 ms                                                        | 1.83 ms: 1.06x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.12 us: 1.06x faster                                                    |
| connected_components             | 208 ms                                                         | 197 ms: 1.05x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 61.3 us: 1.05x faster                                                    |
| pycparser                        | 470 ms                                                         | 447 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.33 us: 1.05x faster                                                    |
| sphinx                           | 409 ms                                                         | 390 ms: 1.05x faster                                                     |
| shortest_path                    | 225 ms                                                         | 215 ms: 1.05x faster                                                     |
| meteor_contest                   | 47.9 ms                                                        | 45.8 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 35.8 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.2 ms: 1.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 962 us: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| raytrace                         | 109 ms                                                         | 106 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| thrift                           | 309 us                                                         | 303 us: 1.02x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.6 ms: 1.01x slower                                                    |
| 2to3                             | 112 ms                                                         | 113 ms: 1.02x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.69 ms: 1.02x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 971 ns: 1.02x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.90 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.12 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.87 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.0 ms: 1.06x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.41 ms: 1.08x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 57.3 ms: 1.10x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 107 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| pylint                           | 106 ms                                                         | 124 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 45.9 ms: 1.21x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.2 ms: 1.22x slower                                                    |
| many_optionals                   | 200 us                                                         | 258 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.1 ms: 2.70x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                             |

Benchmark hidden because not significant (1): genshi_xml
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260110-3.15.0a3+-aa8578d-JIT/bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.151x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.20x