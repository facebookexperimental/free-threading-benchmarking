# Results vs. 3.13.0rc2

- fork: python
- ref: 0bbdb4e897ae909af39c
- machine: darwin-arm64
- commit hash: 0bbdb4e
- commit date: 2026-02-18
- overall geometric mean: 1.012x faster
- HPT reliability: 54.87%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.08x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.0 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 424 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 243 ms: 2.14x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.12x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 236 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 187 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.7 ms: 3.21x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.4 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.2 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 50.8 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.88 ms: 1.20x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 883 ms: 1.13x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 61.2 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.0 ms: 1.16x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.28 ms: 1.22x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.19x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.8 ms: 1.07x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                    |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| mako            | 4.41 ms                                                        | 5.53 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 799 us: 2.55x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 243 ms: 2.14x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.12x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 507 us: 1.96x faster                                                     |
| mdp                              | 1.06 sec                                                       | 612 ms: 1.73x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 236 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.14 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 990 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 107 us: 1.35x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.30x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| go                               | 72.6 ms                                                        | 59.9 ms: 1.21x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 789 ns: 1.20x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.88 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.1 ms: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 883 ms: 1.13x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.11x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| float                            | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                     |
| async_generators                 | 193 ms                                                         | 187 ms: 1.03x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.2 ms: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.03 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 466 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 23.0 ms: 1.01x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.2 ms: 1.01x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 529 ms: 1.01x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 663 ms: 1.02x slower                                                     |
| sphinx                           | 409 ms                                                         | 424 ms: 1.04x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.1 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.8 ms: 1.06x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.8 ms: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.3 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.07x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.40 us: 1.07x slower                                                    |
| thrift                           | 309 us                                                         | 333 us: 1.08x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 43.9 ns: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| 2to3                             | 112 ms                                                         | 121 ms: 1.08x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.5 ms: 1.09x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.19 ms: 1.09x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.68 us: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 72.7 us: 1.12x slower                                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                    |
| shortest_path                    | 225 ms                                                         | 254 ms: 1.13x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 42.5 ms: 1.14x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.8 ms: 1.15x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.4 ms: 1.16x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 10.0 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 51.3 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.5 ms: 1.18x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.18x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.15 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.27 us: 1.22x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.28 ms: 1.22x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.0 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.24x slower                                                     |
| coverage                         | 31.2 ms                                                        | 38.9 ms: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.53 ms: 1.25x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 44.2 ms: 1.31x slower                                                    |
| many_optionals                   | 200 us                                                         | 266 us: 1.33x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 57.4 ms: 1.34x slower                                                    |
| generators                       | 15.7 ms                                                        | 21.1 ms: 1.34x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.4 ms: 1.35x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 575 us: 1.40x slower                                                     |
| connected_components             | 208 ms                                                         | 302 ms: 1.45x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.7 ms: 3.21x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (2): pprint_safe_repr, async_tree_eager_cpu_io_mixed
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260218-3.15.0a6+-0bbdb4e-NOGIL/bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 54.87% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x