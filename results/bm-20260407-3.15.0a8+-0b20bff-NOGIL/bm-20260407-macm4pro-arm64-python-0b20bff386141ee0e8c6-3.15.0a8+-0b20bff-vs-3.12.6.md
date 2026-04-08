# Results vs. 3.12.6

- fork: python
- ref: 0b20bff386141ee0e8c6
- machine: darwin-arm64
- commit hash: 0b20bff
- commit date: 2026-04-07
- overall geometric mean: 1.099x faster
- HPT reliability: 99.63%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| docutils       | 1.02 sec                                                 | 988 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.7 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 418 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.02x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 239 ms: 2.00x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.86x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.60x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 117 ms: 1.53x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| async_generators                 | 206 ms                                                   | 189 ms: 1.09x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.3 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.3 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| nbody          | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.7 ms: 1.08x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.1 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.9 ms: 1.29x faster                                                    |
| tomli_loads          | 957 ms                                                   | 859 ms: 1.12x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 61.3 ms: 1.11x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.93 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.04x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.06x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.70 ms: 1.21x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.06 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.13x slower                                                    |
| mako            | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.11 ms: 5.05x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 796 us: 2.52x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.02x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 239 ms: 2.00x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.86x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                     |
| mdp                              | 1.09 sec                                                 | 605 ms: 1.80x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 510 us: 1.63x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.60x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 117 ms: 1.53x faster                                                     |
| deepcopy                         | 161 us                                                   | 107 us: 1.50x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                    |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.9 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 781 ns: 1.24x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.17 us: 1.20x faster                                                    |
| go                               | 70.0 ms                                                  | 59.2 ms: 1.18x faster                                                    |
| pylint                           | 128 ms                                                   | 110 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.6 ns: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 991 ms: 1.13x faster                                                     |
| pyflate                          | 216 ms                                                   | 192 ms: 1.12x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 859 ms: 1.12x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 61.3 ms: 1.11x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.10x faster                                                    |
| pycparser                        | 497 ms                                                   | 455 ms: 1.09x faster                                                     |
| async_generators                 | 206 ms                                                   | 189 ms: 1.09x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.57 us: 1.09x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.93 ms: 1.08x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 50.7 ms: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.7 ms: 1.07x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.6 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.2 ms: 1.06x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| sphinx                           | 434 ms                                                   | 418 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.04x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 96.1 ms: 1.04x faster                                                    |
| docutils                         | 1.02 sec                                                 | 988 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.7 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 330 ms: 1.01x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 673 ms: 1.01x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.7 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.7 us: 1.02x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.13 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.16 ms: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.3 ms: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.3 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 53.9 ms: 1.05x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.7 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.6 ms: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.06x slower                                                     |
| thrift                           | 322 us                                                   | 343 us: 1.06x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                     |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.12x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 44.1 ms: 1.13x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                     |
| shortest_path                    | 219 ms                                                   | 251 ms: 1.14x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 54.8 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 46.8 ms: 1.18x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.70 ms: 1.21x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.06 ms: 1.24x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 568 us: 1.36x slower                                                     |
| many_optionals                   | 195 us                                                   | 267 us: 1.37x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.9 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.3 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (5): fannkuch, sympy_integrate, dask, scimark_sor, json
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260407-3.15.0a8+-0b20bff-NOGIL/bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.099x faster

# HPT report

- Reliability score: 99.63% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.38x