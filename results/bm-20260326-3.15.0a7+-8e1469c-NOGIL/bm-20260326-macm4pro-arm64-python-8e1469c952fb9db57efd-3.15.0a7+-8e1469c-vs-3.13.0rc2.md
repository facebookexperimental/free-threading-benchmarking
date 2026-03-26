# Results vs. 3.13.0rc2

- fork: python
- ref: 8e1469c952fb9db57efd
- machine: darwin-arm64
- commit hash: 8e1469c
- commit date: 2026-03-26
- overall geometric mean: 1.019x faster
- HPT reliability: 53.84%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| docutils       | 1.05 sec                                                       | 995 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 415 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 240 ms: 2.17x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.14x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| async_generators                 | 193 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.0 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.8 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.5 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.16 ms: 1.17x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 51.0 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.0 ms: 1.18x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 850 ms: 1.18x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 56.7 ms: 1.10x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.75 ms: 1.13x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.07 ms: 1.19x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.7 ms: 1.06x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.0 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| mako            | 4.41 ms                                                        | 5.53 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 794 us: 2.57x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 240 ms: 2.17x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.14x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 508 us: 1.96x faster                                                     |
| mdp                              | 1.06 sec                                                       | 599 ms: 1.76x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.12 ms: 1.52x faster                                                    |
| k_core                           | 1.46 sec                                                       | 991 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 106 us: 1.37x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.31x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| go                               | 72.6 ms                                                        | 59.7 ms: 1.22x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 792 ns: 1.20x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.0 ms: 1.18x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 850 ms: 1.18x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.16 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.1 ms: 1.16x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.12x faster                                                    |
| float                            | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 56.7 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                    |
| docutils                         | 1.05 sec                                                       | 995 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| pycparser                        | 470 ms                                                         | 458 ms: 1.03x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| async_generators                 | 193 ms                                                         | 189 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| dask                             | 525 ms                                                         | 529 ms: 1.01x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 326 ms: 1.01x slower                                                     |
| sphinx                           | 409 ms                                                         | 415 ms: 1.02x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.02x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 665 ms: 1.02x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.59 us: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.7 ms: 1.06x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.0 ms: 1.06x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.6 ms: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.13 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.0 ms: 1.09x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.7 ms: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.7 ns: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| thrift                           | 309 us                                                         | 341 us: 1.10x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 27.2 ms: 1.10x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.0 ms: 1.10x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.0 ms: 1.11x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 250 ms: 1.11x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.12x slower                                                     |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.75 ms: 1.13x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.6 ms: 1.14x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.5 us: 1.14x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 49.9 ms: 1.14x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.66 ms: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.6 ms: 1.16x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.3 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.17x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.07 ms: 1.19x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.17 ms: 1.22x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.32 us: 1.22x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.6 ms: 1.23x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.7 ms: 1.24x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.53 ms: 1.25x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 54.7 ms: 1.28x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 43.7 ms: 1.30x slower                                                    |
| many_optionals                   | 200 us                                                         | 269 us: 1.34x slower                                                     |
| generators                       | 15.7 ms                                                        | 21.2 ms: 1.35x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.5 ms: 1.35x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 569 us: 1.38x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.8 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (3): json, regex_dna, fannkuch
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260326-3.15.0a7+-8e1469c-NOGIL/bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.019x faster

# HPT report

- Reliability score: 53.84% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.33x