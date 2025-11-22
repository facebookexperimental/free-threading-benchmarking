# Results vs. 3.12.6

- fork: python
- ref: 92972aea0f0e12dd21bf
- machine: darwin-arm64
- commit hash: 92972ae
- commit date: 2025-11-21
- overall geometric mean: 1.104x faster
- HPT reliability: 99.85%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| docutils       | 1.02 sec                                                 | 999 ms: 1.02x faster                                                     |
| sphinx         | 434 ms                                                   | 421 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x faster                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 200 ms: 2.48x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.43x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 191 ms: 2.33x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.1 ms: 2.02x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 122 ms: 1.89x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 97.9 ms: 1.82x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.73x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.6 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.6 ms: 2.38x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.39x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.6 ms: 1.38x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| nbody          | 54.2 ms                                                  | 55.8 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.8 ms: 1.05x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.5 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.32 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.5 ms: 1.27x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.3 ms: 1.11x faster                                                    |
| tomli_loads          | 957 ms                                                   | 871 ms: 1.10x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.99 ms: 1.07x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.85 ms: 1.23x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.15 ms: 1.25x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.24x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.0 ms: 1.05x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| mako            | 4.77 ms                                                  | 5.51 ms: 1.15x slower                                                    |
| django_template | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.11x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 773 us: 2.60x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 200 ms: 2.48x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.43x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 191 ms: 2.33x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.1 ms: 2.02x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 122 ms: 1.89x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 97.9 ms: 1.82x faster                                                    |
| mdp                              | 1.09 sec                                                 | 608 ms: 1.80x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 479 us: 1.73x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.73x faster                                                     |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                     |
| float                            | 37.9 ms                                                  | 27.6 ms: 1.38x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.5 ms: 1.27x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.19 us: 1.23x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.08 us: 1.22x faster                                                    |
| go                               | 70.0 ms                                                  | 59.1 ms: 1.19x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.2 ns: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 830 ns: 1.17x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.6 ms: 1.12x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 18.6 ms: 1.12x faster                                                    |
| pyflate                          | 216 ms                                                   | 193 ms: 1.12x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 61.3 ms: 1.11x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.4 ms: 1.10x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 871 ms: 1.10x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.59 ms: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.3 ms: 1.08x faster                                                    |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.99 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 467 ms: 1.07x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.8 ms: 1.05x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.45 us: 1.05x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.6 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.71 us: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.5 ms: 1.03x faster                                                    |
| sphinx                           | 434 ms                                                   | 421 ms: 1.03x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.32 ms: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 171 ms: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 999 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.02x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 43.0 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.11 ms: 1.01x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.08 ms: 1.01x slower                                                    |
| richards                         | 22.4 ms                                                  | 22.7 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 335 ms: 1.02x slower                                                     |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| thrift                           | 322 us                                                   | 329 us: 1.02x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.6 ms: 1.02x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.1 ms: 1.03x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 684 ms: 1.03x slower                                                     |
| nbody                            | 54.2 ms                                                  | 55.8 ms: 1.03x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.3 ms: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.6 ms: 1.05x slower                                                    |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.0 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                     |
| dask                             | 528 ms                                                   | 560 ms: 1.06x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.5 ms: 1.09x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.29 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.99 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.51 ms: 1.15x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.1 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.5 ms: 1.16x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 61.1 ms: 1.19x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.85 ms: 1.23x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.15 ms: 1.25x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 566 us: 1.35x slower                                                     |
| coverage                         | 26.9 ms                                                  | 39.3 ms: 1.46x slower                                                    |
| many_optionals                   | 195 us                                                   | 378 us: 1.93x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.6 ms: 2.38x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (3): html5lib, xml_etree_process, typing_runtime_protocols
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251121-3.15.0a2+-92972ae-NOGIL/bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.104x faster

# HPT report

- Reliability score: 99.85% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.36x