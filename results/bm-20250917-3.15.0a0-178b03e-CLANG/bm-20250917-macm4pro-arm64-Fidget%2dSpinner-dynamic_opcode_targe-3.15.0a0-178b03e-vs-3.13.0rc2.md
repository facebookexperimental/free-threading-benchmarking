# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: dynamic_opcode_targe
- machine: darwin-arm64
- commit hash: 178b03e
- commit date: 2025-09-17
- overall geometric mean: 1.064x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 108 ms: 1.04x faster                                                              |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                            |
| html5lib       | 23.1 ms                                                        | 21.9 ms: 1.05x faster                                                             |
| sphinx         | 409 ms                                                         | 401 ms: 1.02x faster                                                              |
| Geometric mean | (ref)                                                          | 1.03x faster                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 235 ms: 2.24x faster                                                              |
| async_tree_eager_io_tg           | 521 ms                                                         | 240 ms: 2.17x faster                                                              |
| async_tree_io_tg                 | 405 ms                                                         | 242 ms: 1.68x faster                                                              |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.58x faster                                                              |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                              |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.30x faster                                                              |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                              |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.28x faster                                                              |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                              |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 257 ms: 1.14x faster                                                              |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                              |
| async_generators                 | 193 ms                                                         | 169 ms: 1.14x faster                                                              |
| async_tree_eager                 | 43.2 ms                                                        | 38.8 ms: 1.11x faster                                                             |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                             |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                              |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                              |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                              |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.23x slower                                                              |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.3 ms: 2.88x slower                                                             |
| Geometric mean                   | (ref)                                                          | 1.17x faster                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                             |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                              |
| nbody          | 42.5 ms                                                        | 48.5 ms: 1.14x slower                                                             |
| Geometric mean | (ref)                                                          | 1.01x slower                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.5 ms: 1.10x faster                                                             |
| regex_v8       | 10.7 ms                                                        | 11.2 ms: 1.04x slower                                                             |
| regex_effbot   | 1.61 ms                                                        | 1.74 ms: 1.08x slower                                                             |
| regex_dna      | 94.6 ms                                                        | 104 ms: 1.10x slower                                                              |
| Geometric mean | (ref)                                                          | 1.03x slower                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 778 ms: 1.29x faster                                                              |
| json_dumps           | 4.65 ms                                                        | 3.68 ms: 1.27x faster                                                             |
| unpickle_pure_python | 99.5 us                                                        | 91.4 us: 1.09x faster                                                             |
| xml_etree_generate   | 35.8 ms                                                        | 32.9 ms: 1.09x faster                                                             |
| xml_etree_process    | 25.4 ms                                                        | 23.8 ms: 1.07x faster                                                             |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.3 ms: 1.04x faster                                                             |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.02x faster                                                             |
| pickle_pure_python   | 130 us                                                         | 134 us: 1.03x slower                                                              |
| xml_etree_parse      | 62.4 ms                                                        | 64.6 ms: 1.03x slower                                                             |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.59 ms: 1.01x faster                                                             |
| python_startup_no_site | 5.95 ms                                                        | 6.15 ms: 1.03x slower                                                             |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.06 ms: 1.10x faster                                                             |
| genshi_xml      | 21.4 ms                                                        | 19.5 ms: 1.10x faster                                                             |
| mako            | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                             |
| django_template | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                             |
| Geometric mean  | (ref)                                                          | 1.00x faster                                                                      |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 235 ms: 2.24x faster                                                              |
| async_tree_eager_io_tg           | 521 ms                                                         | 240 ms: 2.17x faster                                                              |
| mdp                              | 1.06 sec                                                       | 520 ms: 2.04x faster                                                              |
| async_tree_io_tg                 | 405 ms                                                         | 242 ms: 1.68x faster                                                              |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.58x faster                                                              |
| k_core                           | 1.46 sec                                                       | 942 ms: 1.55x faster                                                              |
| deepcopy                         | 145 us                                                         | 97.3 us: 1.49x faster                                                             |
| deepcopy_memo                    | 16.5 us                                                        | 11.2 us: 1.47x faster                                                             |
| go                               | 72.6 ms                                                        | 50.6 ms: 1.43x faster                                                             |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                              |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.30x faster                                                              |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                              |
| tomli_loads                      | 1000 ms                                                        | 778 ms: 1.29x faster                                                              |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.28x faster                                                              |
| json_dumps                       | 4.65 ms                                                        | 3.68 ms: 1.27x faster                                                             |
| scimark_sor                      | 64.0 ms                                                        | 51.2 ms: 1.25x faster                                                             |
| deepcopy_reduce                  | 1.30 us                                                        | 1.05 us: 1.23x faster                                                             |
| pyflate                          | 222 ms                                                         | 186 ms: 1.19x faster                                                              |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                              |
| dulwich_log                      | 19.8 ms                                                        | 17.1 ms: 1.16x faster                                                             |
| richards                         | 22.1 ms                                                        | 19.2 ms: 1.15x faster                                                             |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 257 ms: 1.14x faster                                                              |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                              |
| async_generators                 | 193 ms                                                         | 169 ms: 1.14x faster                                                              |
| richards_super                   | 24.7 ms                                                        | 21.8 ms: 1.13x faster                                                             |
| hexiom                           | 2.85 ms                                                        | 2.55 ms: 1.11x faster                                                             |
| telco                            | 3.07 ms                                                        | 2.75 ms: 1.11x faster                                                             |
| async_tree_eager                 | 43.2 ms                                                        | 38.8 ms: 1.11x faster                                                             |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                            |
| generators                       | 15.7 ms                                                        | 14.2 ms: 1.10x faster                                                             |
| regex_compile                    | 47.9 ms                                                        | 43.5 ms: 1.10x faster                                                             |
| genshi_text                      | 9.97 ms                                                        | 9.06 ms: 1.10x faster                                                             |
| genshi_xml                       | 21.4 ms                                                        | 19.5 ms: 1.10x faster                                                             |
| unpickle_pure_python             | 99.5 us                                                        | 91.4 us: 1.09x faster                                                             |
| xml_etree_generate               | 35.8 ms                                                        | 32.9 ms: 1.09x faster                                                             |
| create_gc_cycles                 | 993 us                                                         | 919 us: 1.08x faster                                                              |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                             |
| float                            | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                             |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                             |
| xml_etree_process                | 25.4 ms                                                        | 23.8 ms: 1.07x faster                                                             |
| typing_runtime_protocols         | 64.6 us                                                        | 60.7 us: 1.07x faster                                                             |
| logging_format                   | 2.45 us                                                        | 2.32 us: 1.05x faster                                                             |
| html5lib                         | 23.1 ms                                                        | 21.9 ms: 1.05x faster                                                             |
| thrift                           | 309 us                                                         | 293 us: 1.05x faster                                                              |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                              |
| pprint_pformat                   | 650 ms                                                         | 618 ms: 1.05x faster                                                              |
| sympy_integrate                  | 7.53 ms                                                        | 7.17 ms: 1.05x faster                                                             |
| logging_silent                   | 40.6 ns                                                        | 38.7 ns: 1.05x faster                                                             |
| pprint_safe_repr                 | 322 ms                                                         | 308 ms: 1.05x faster                                                              |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.3 ms: 1.04x faster                                                             |
| bench_thread_pool                | 412 us                                                         | 396 us: 1.04x faster                                                              |
| logging_simple                   | 2.24 us                                                        | 2.16 us: 1.04x faster                                                             |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                              |
| 2to3                             | 112 ms                                                         | 108 ms: 1.04x faster                                                              |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                             |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                              |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.1 ms: 1.03x faster                                                             |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                              |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                              |
| sphinx                           | 409 ms                                                         | 401 ms: 1.02x faster                                                              |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.02x faster                                                             |
| sympy_expand                     | 159 ms                                                         | 157 ms: 1.01x faster                                                              |
| sqlite_synth                     | 948 ns                                                         | 937 ns: 1.01x faster                                                              |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                              |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                            |
| sympy_str                        | 95.5 ms                                                        | 94.4 ms: 1.01x faster                                                             |
| gc_traversal                     | 2.04 ms                                                        | 2.03 ms: 1.01x faster                                                             |
| python_startup                   | 8.63 ms                                                        | 8.59 ms: 1.01x faster                                                             |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                              |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.01x slower                                                             |
| meteor_contest                   | 47.9 ms                                                        | 48.3 ms: 1.01x slower                                                             |
| sympy_sum                        | 52.3 ms                                                        | 52.8 ms: 1.01x slower                                                             |
| comprehensions                   | 6.80 us                                                        | 6.88 us: 1.01x slower                                                             |
| nqueens                          | 37.2 ms                                                        | 37.7 ms: 1.01x slower                                                             |
| coverage                         | 31.2 ms                                                        | 32.0 ms: 1.03x slower                                                             |
| pylint                           | 106 ms                                                         | 108 ms: 1.03x slower                                                              |
| pickle_pure_python               | 130 us                                                         | 134 us: 1.03x slower                                                              |
| spectral_norm                    | 43.7 ms                                                        | 45.1 ms: 1.03x slower                                                             |
| python_startup_no_site           | 5.95 ms                                                        | 6.15 ms: 1.03x slower                                                             |
| xml_etree_parse                  | 62.4 ms                                                        | 64.6 ms: 1.03x slower                                                             |
| regex_v8                         | 10.7 ms                                                        | 11.2 ms: 1.04x slower                                                             |
| chaos                            | 24.3 ms                                                        | 25.4 ms: 1.05x slower                                                             |
| raytrace                         | 109 ms                                                         | 115 ms: 1.05x slower                                                              |
| scimark_lu                       | 42.8 ms                                                        | 45.2 ms: 1.06x slower                                                             |
| mako                             | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                             |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.06x slower                                                              |
| regex_effbot                     | 1.61 ms                                                        | 1.74 ms: 1.08x slower                                                             |
| crypto_pyaes                     | 33.6 ms                                                        | 36.6 ms: 1.09x slower                                                             |
| bench_mp_pool                    | 37.8 ms                                                        | 41.2 ms: 1.09x slower                                                             |
| regex_dna                        | 94.6 ms                                                        | 104 ms: 1.10x slower                                                              |
| django_template                  | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                             |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.01 ms: 1.13x slower                                                             |
| nbody                            | 42.5 ms                                                        | 48.5 ms: 1.14x slower                                                             |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                              |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.23x slower                                                              |
| many_optionals                   | 200 us                                                         | 306 us: 1.52x slower                                                              |
| subparsers                       | 6.26 ms                                                        | 17.0 ms: 2.71x slower                                                             |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.3 ms: 2.88x slower                                                             |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                                      |

Benchmark hidden because not significant (1): pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250917-3.15.0a0-178b03e-CLANG/bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.064x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.09x