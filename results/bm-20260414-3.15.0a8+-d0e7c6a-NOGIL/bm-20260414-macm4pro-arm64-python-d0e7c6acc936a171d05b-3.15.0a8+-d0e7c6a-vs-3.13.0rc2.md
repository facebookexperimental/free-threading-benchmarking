# Results vs. 3.13.0rc2

- fork: python
- ref: d0e7c6acc936a171d05b
- machine: darwin-arm64
- commit hash: d0e7c6a
- commit date: 2026-04-14
- overall geometric mean: 1.020x faster
- HPT reliability: 51.92%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                     |
| docutils       | 1.05 sec                                                       | 998 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 23.0 ms: 1.00x faster                                                    |
| sphinx         | 409 ms                                                         | 422 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 242 ms: 2.15x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.68x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.22x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.6 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.7 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmark hidden because not significant (2): coroutines, async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.6 ms: 1.36x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.30 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.3 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.84 ms: 1.21x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 891 ms: 1.12x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 61.5 ms: 1.01x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.11x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.14x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.62 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.71 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.0 ms: 1.08x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.14x slower                                                    |
| django_template | 12.5 ms                                                        | 15.8 ms: 1.27x slower                                                    |
| mako            | 4.41 ms                                                        | 5.63 ms: 1.28x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 807 us: 2.53x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 242 ms: 2.15x faster                                                     |
| pylint                           | 106 ms                                                         | 51.8 ms: 2.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 513 us: 1.94x faster                                                     |
| mdp                              | 1.06 sec                                                       | 617 ms: 1.71x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.68x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.13 ms: 1.52x faster                                                    |
| k_core                           | 1.46 sec                                                       | 987 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.22x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.84 ms: 1.21x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.21x faster                                                     |
| go                               | 72.6 ms                                                        | 60.1 ms: 1.21x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 792 ns: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.5 ms: 1.15x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.30 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 891 ms: 1.12x faster                                                     |
| float                            | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 998 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                     |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| pycparser                        | 470 ms                                                         | 461 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.5 ms: 1.01x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 23.0 ms: 1.00x faster                                                    |
| dask                             | 525 ms                                                         | 529 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 422 ms: 1.03x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 334 ms: 1.04x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 684 ms: 1.05x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.4 ms: 1.06x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.38 us: 1.07x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.3 ms: 1.07x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.0 ms: 1.08x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.64 us: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.14 ms: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.2 ns: 1.09x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.9 ms: 1.09x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.1 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.6 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.11x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.3 ms: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 250 ms: 1.11x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.62 ms: 1.11x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.18 ms: 1.12x slower                                                    |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                     |
| thrift                           | 309 us                                                         | 347 us: 1.12x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.71 ms: 1.13x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.4 ms: 1.13x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.2 us: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.13x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.14x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.14x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 50.6 ms: 1.16x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.9 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.8 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                     |
| connected_components             | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.16 us: 1.20x slower                                                    |
| coverage                         | 31.2 ms                                                        | 39.1 ms: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.8 ms: 1.27x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 48.1 ms: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.63 ms: 1.28x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 55.2 ms: 1.29x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.30 ms: 1.29x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 44.5 ms: 1.32x slower                                                    |
| generators                       | 15.7 ms                                                        | 21.2 ms: 1.35x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.6 ms: 1.36x slower                                                    |
| many_optionals                   | 200 us                                                         | 272 us: 1.36x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 567 us: 1.38x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.7 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (2): coroutines, async_tree_eager_cpu_io_mixed
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260414-3.15.0a8+-d0e7c6a-NOGIL/bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.020x faster

# HPT report

- Reliability score: 51.92% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.32x