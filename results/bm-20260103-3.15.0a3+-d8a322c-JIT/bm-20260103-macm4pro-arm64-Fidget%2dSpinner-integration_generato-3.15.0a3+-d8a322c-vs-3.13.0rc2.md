# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: integration_generato
- machine: darwin-arm64
- commit hash: d8a322c
- commit date: 2026-01-03
- overall geometric mean: 1.155x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.01x faster                                                               |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                             |
| html5lib       | 23.1 ms                                                        | 20.2 ms: 1.14x faster                                                              |
| sphinx         | 409 ms                                                         | 394 ms: 1.04x faster                                                               |
| Geometric mean | (ref)                                                          | 1.06x faster                                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 220 ms: 2.39x faster                                                               |
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                               |
| async_tree_io_tg                 | 405 ms                                                         | 219 ms: 1.85x faster                                                               |
| async_tree_io                    | 386 ms                                                         | 226 ms: 1.71x faster                                                               |
| async_tree_none                  | 142 ms                                                         | 96.2 ms: 1.48x faster                                                              |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.38x faster                                                               |
| async_tree_none_tg               | 133 ms                                                         | 96.4 ms: 1.38x faster                                                              |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.36x faster                                                               |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                               |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                               |
| async_tree_eager                 | 43.2 ms                                                        | 36.9 ms: 1.17x faster                                                              |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 215 ms: 1.04x faster                                                               |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                              |
| async_generators                 | 193 ms                                                         | 192 ms: 1.00x faster                                                               |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.14x slower                                                               |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                               |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.9 ms: 2.69x slower                                                              |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 23.0 ms: 1.37x faster                                                              |
| nbody          | 42.5 ms                                                        | 40.1 ms: 1.06x faster                                                              |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                               |
| Geometric mean | (ref)                                                          | 1.14x faster                                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 40.8 ms: 1.18x faster                                                              |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                              |
| regex_v8       | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                              |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                       |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|----------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| unpickle_pure_python | 99.5 us                                                        | 72.3 us: 1.38x faster                                                              |
| tomli_loads          | 1000 ms                                                        | 780 ms: 1.28x faster                                                               |
| json_dumps           | 4.65 ms                                                        | 3.66 ms: 1.27x faster                                                              |
| xml_etree_iterparse  | 46.1 ms                                                        | 37.9 ms: 1.22x faster                                                              |
| pickle_pure_python   | 130 us                                                         | 112 us: 1.17x faster                                                               |
| xml_etree_generate   | 35.8 ms                                                        | 31.0 ms: 1.15x faster                                                              |
| xml_etree_process    | 25.4 ms                                                        | 22.0 ms: 1.15x faster                                                              |
| xml_etree_parse      | 62.4 ms                                                        | 61.0 ms: 1.02x faster                                                              |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                              |
| Geometric mean       | (ref)                                                          | 1.18x faster                                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.84 ms: 1.02x slower                                                              |
| python_startup_no_site | 5.95 ms                                                        | 6.37 ms: 1.07x slower                                                              |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|-----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 8.75 ms: 1.14x faster                                                              |
| mako            | 4.41 ms                                                        | 3.93 ms: 1.12x faster                                                              |
| genshi_xml      | 21.4 ms                                                        | 20.3 ms: 1.05x faster                                                              |
| django_template | 12.5 ms                                                        | 13.9 ms: 1.11x slower                                                              |
| Geometric mean  | (ref)                                                          | 1.05x faster                                                                       |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 220 ms: 2.39x faster                                                               |
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                               |
| richards                         | 22.1 ms                                                        | 9.85 ms: 2.24x faster                                                              |
| richards_super                   | 24.7 ms                                                        | 11.6 ms: 2.14x faster                                                              |
| async_tree_io_tg                 | 405 ms                                                         | 219 ms: 1.85x faster                                                               |
| mdp                              | 1.06 sec                                                       | 587 ms: 1.80x faster                                                               |
| async_tree_io                    | 386 ms                                                         | 226 ms: 1.71x faster                                                               |
| k_core                           | 1.46 sec                                                       | 865 ms: 1.69x faster                                                               |
| go                               | 72.6 ms                                                        | 43.2 ms: 1.68x faster                                                              |
| subparsers                       | 6.26 ms                                                        | 3.92 ms: 1.60x faster                                                              |
| pyflate                          | 222 ms                                                         | 144 ms: 1.54x faster                                                               |
| scimark_sor                      | 64.0 ms                                                        | 42.1 ms: 1.52x faster                                                              |
| deepcopy                         | 145 us                                                         | 96.7 us: 1.50x faster                                                              |
| async_tree_none                  | 142 ms                                                         | 96.2 ms: 1.48x faster                                                              |
| deepcopy_memo                    | 16.5 us                                                        | 11.3 us: 1.46x faster                                                              |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.38x faster                                                               |
| unpickle_pure_python             | 99.5 us                                                        | 72.3 us: 1.38x faster                                                              |
| async_tree_none_tg               | 133 ms                                                         | 96.4 ms: 1.38x faster                                                              |
| float                            | 31.4 ms                                                        | 23.0 ms: 1.37x faster                                                              |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.36x faster                                                               |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.0 ms: 1.36x faster                                                              |
| deepcopy_reduce                  | 1.30 us                                                        | 965 ns: 1.34x faster                                                               |
| tomli_loads                      | 1000 ms                                                        | 780 ms: 1.28x faster                                                               |
| deltablue                        | 1.45 ms                                                        | 1.13 ms: 1.28x faster                                                              |
| json_dumps                       | 4.65 ms                                                        | 3.66 ms: 1.27x faster                                                              |
| pprint_safe_repr                 | 322 ms                                                         | 256 ms: 1.26x faster                                                               |
| pprint_pformat                   | 650 ms                                                         | 521 ms: 1.25x faster                                                               |
| scimark_fft                      | 124 ms                                                         | 101 ms: 1.22x faster                                                               |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                               |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.9 ms: 1.22x faster                                                              |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                               |
| telco                            | 3.07 ms                                                        | 2.58 ms: 1.19x faster                                                              |
| logging_silent                   | 40.6 ns                                                        | 34.4 ns: 1.18x faster                                                              |
| regex_compile                    | 47.9 ms                                                        | 40.8 ms: 1.18x faster                                                              |
| async_tree_eager                 | 43.2 ms                                                        | 36.9 ms: 1.17x faster                                                              |
| pickle_pure_python               | 130 us                                                         | 112 us: 1.17x faster                                                               |
| fannkuch                         | 179 ms                                                         | 153 ms: 1.16x faster                                                               |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.84 sec: 1.16x faster                                                             |
| scimark_lu                       | 42.8 ms                                                        | 37.0 ms: 1.16x faster                                                              |
| xml_etree_generate               | 35.8 ms                                                        | 31.0 ms: 1.15x faster                                                              |
| xml_etree_process                | 25.4 ms                                                        | 22.0 ms: 1.15x faster                                                              |
| html5lib                         | 23.1 ms                                                        | 20.2 ms: 1.14x faster                                                              |
| genshi_text                      | 9.97 ms                                                        | 8.75 ms: 1.14x faster                                                              |
| mako                             | 4.41 ms                                                        | 3.93 ms: 1.12x faster                                                              |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                              |
| comprehensions                   | 6.80 us                                                        | 6.17 us: 1.10x faster                                                              |
| chaos                            | 24.3 ms                                                        | 22.2 ms: 1.09x faster                                                              |
| regex_v8                         | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                              |
| crypto_pyaes                     | 33.6 ms                                                        | 30.9 ms: 1.09x faster                                                              |
| hexiom                           | 2.85 ms                                                        | 2.65 ms: 1.08x faster                                                              |
| create_gc_cycles                 | 993 us                                                         | 931 us: 1.07x faster                                                               |
| spectral_norm                    | 43.7 ms                                                        | 41.0 ms: 1.07x faster                                                              |
| nbody                            | 42.5 ms                                                        | 40.1 ms: 1.06x faster                                                              |
| logging_simple                   | 2.24 us                                                        | 2.11 us: 1.06x faster                                                              |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.06x faster                                                              |
| pycparser                        | 470 ms                                                         | 445 ms: 1.06x faster                                                               |
| genshi_xml                       | 21.4 ms                                                        | 20.3 ms: 1.05x faster                                                              |
| json                             | 1.94 ms                                                        | 1.84 ms: 1.05x faster                                                              |
| connected_components             | 208 ms                                                         | 198 ms: 1.05x faster                                                               |
| logging_format                   | 2.45 us                                                        | 2.33 us: 1.05x faster                                                              |
| typing_runtime_protocols         | 64.6 us                                                        | 61.8 us: 1.05x faster                                                              |
| shortest_path                    | 225 ms                                                         | 215 ms: 1.04x faster                                                               |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 215 ms: 1.04x faster                                                               |
| sphinx                           | 409 ms                                                         | 394 ms: 1.04x faster                                                               |
| meteor_contest                   | 47.9 ms                                                        | 46.2 ms: 1.04x faster                                                              |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                              |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                             |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                              |
| xml_etree_parse                  | 62.4 ms                                                        | 61.0 ms: 1.02x faster                                                              |
| raytrace                         | 109 ms                                                         | 107 ms: 1.02x faster                                                               |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                              |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                               |
| thrift                           | 309 us                                                         | 305 us: 1.01x faster                                                               |
| 2to3                             | 112 ms                                                         | 110 ms: 1.01x faster                                                               |
| async_generators                 | 193 ms                                                         | 192 ms: 1.00x faster                                                               |
| sympy_integrate                  | 7.53 ms                                                        | 7.63 ms: 1.01x slower                                                              |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                              |
| python_startup                   | 8.63 ms                                                        | 8.84 ms: 1.02x slower                                                              |
| sqlite_synth                     | 948 ns                                                         | 974 ns: 1.03x slower                                                               |
| nqueens                          | 37.2 ms                                                        | 38.4 ms: 1.03x slower                                                              |
| bench_thread_pool                | 412 us                                                         | 426 us: 1.04x slower                                                               |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.87 ms: 1.05x slower                                                              |
| coverage                         | 31.2 ms                                                        | 33.1 ms: 1.06x slower                                                              |
| python_startup_no_site           | 5.95 ms                                                        | 6.37 ms: 1.07x slower                                                              |
| sympy_sum                        | 52.3 ms                                                        | 56.5 ms: 1.08x slower                                                              |
| sympy_expand                     | 159 ms                                                         | 175 ms: 1.10x slower                                                               |
| sympy_str                        | 95.5 ms                                                        | 106 ms: 1.11x slower                                                               |
| django_template                  | 12.5 ms                                                        | 13.9 ms: 1.11x slower                                                              |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.14x slower                                                               |
| pylint                           | 106 ms                                                         | 122 ms: 1.16x slower                                                               |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                               |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.19x slower                                                              |
| bench_mp_pool                    | 37.8 ms                                                        | 45.1 ms: 1.19x slower                                                              |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                               |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.9 ms: 2.69x slower                                                              |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                                       |

Benchmark hidden because not significant (1): regex_dna
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: async_tree_eager_memoization, asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260103-3.15.0a3+-d8a322c-JIT/bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.155x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.21x