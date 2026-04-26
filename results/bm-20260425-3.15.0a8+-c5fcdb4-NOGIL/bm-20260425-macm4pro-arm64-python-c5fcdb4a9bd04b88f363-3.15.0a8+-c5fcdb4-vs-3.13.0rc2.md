# Results vs. 3.13.0rc2

- fork: python
- ref: c5fcdb4a9bd04b88f363
- machine: darwin-arm64
- commit hash: c5fcdb4
- commit date: 2026-04-25
- overall geometric mean: 1.023x faster
- HPT reliability: 60.82%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                     |
| docutils       | 1.05 sec                                                       | 995 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 23.0 ms: 1.00x faster                                                    |
| sphinx         | 409 ms                                                         | 420 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 241 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 252 ms: 1.61x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.22x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 185 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.3 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.2 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.5 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.2 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.1 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 886 ms: 1.13x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.3 ms: 1.07x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 150 us: 1.15x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.59 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.70 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.1 ms: 1.08x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 12.1 ms: 1.21x slower                                                    |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                    |
| mako            | 4.41 ms                                                        | 5.70 ms: 1.29x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 815 us: 2.50x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 241 ms: 2.16x faster                                                     |
| pylint                           | 106 ms                                                         | 51.7 ms: 2.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 520 us: 1.91x faster                                                     |
| mdp                              | 1.06 sec                                                       | 616 ms: 1.72x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 252 ms: 1.61x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.14 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 997 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 107 us: 1.36x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.22x faster                                                     |
| go                               | 72.6 ms                                                        | 59.6 ms: 1.22x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.21x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 807 ns: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 56.0 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 886 ms: 1.13x faster                                                     |
| float                            | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.3 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 995 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 185 ms: 1.04x faster                                                     |
| fannkuch                         | 179 ms                                                         | 173 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| pycparser                        | 470 ms                                                         | 459 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.04 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 23.0 ms: 1.00x faster                                                    |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.2 ms: 1.01x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 127 ms: 1.03x slower                                                     |
| sphinx                           | 409 ms                                                         | 420 ms: 1.03x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 336 ms: 1.05x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.59 us: 1.06x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.4 ms: 1.06x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 690 ms: 1.06x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 51.1 ms: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.6 ms: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.11 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.1 ms: 1.08x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.3 ms: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.4 ns: 1.09x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.0 ms: 1.10x slower                                                    |
| shortest_path                    | 225 ms                                                         | 248 ms: 1.10x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.59 ms: 1.11x slower                                                    |
| thrift                           | 309 us                                                         | 344 us: 1.11x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.17 ms: 1.11x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.6 ms: 1.12x slower                                                    |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 72.4 us: 1.12x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.3 ms: 1.13x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.70 ms: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 50.4 ms: 1.15x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 150 us: 1.15x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.8 ms: 1.16x slower                                                    |
| raytrace                         | 109 ms                                                         | 127 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.8 ms: 1.17x slower                                                    |
| connected_components             | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.17 us: 1.20x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 12.1 ms: 1.21x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.16 ms: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 54.0 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| coverage                         | 31.2 ms                                                        | 39.7 ms: 1.27x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 48.2 ms: 1.28x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.70 ms: 1.29x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 44.3 ms: 1.32x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.5 ms: 1.33x slower                                                    |
| many_optionals                   | 200 us                                                         | 268 us: 1.34x slower                                                     |
| generators                       | 15.7 ms                                                        | 21.1 ms: 1.34x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 569 us: 1.38x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.2 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (1): json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260425-3.15.0a8+-c5fcdb4-NOGIL/bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.023x faster

# HPT report

- Reliability score: 60.82% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.33x