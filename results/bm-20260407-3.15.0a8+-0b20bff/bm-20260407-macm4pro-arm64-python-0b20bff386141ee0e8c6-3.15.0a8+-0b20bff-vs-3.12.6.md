# Results vs. 3.12.6

- fork: python
- ref: 0b20bff386141ee0e8c6
- machine: darwin-arm64
- commit hash: 0b20bff
- commit date: 2026-04-07
- overall geometric mean: 1.172x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| docutils       | 1.02 sec                                                 | 998 ms: 1.02x faster                                                     |
| html5lib       | 23.0 ms                                                  | 21.2 ms: 1.09x faster                                                    |
| sphinx         | 434 ms                                                   | 392 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 217 ms: 2.06x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 229 ms: 2.00x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.5 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 99.5 ms: 1.73x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.70x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.63x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 249 ms: 1.34x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.26x faster                                                     |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 39.7 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.11x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.5 ms: 2.51x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.6 ms: 1.42x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.0 ms: 1.23x faster                                                    |
| Geometric mean | (ref)                                                    | 1.21x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.7 ms: 1.19x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.7 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.6 ms: 1.30x faster                                                    |
| tomli_loads          | 957 ms                                                   | 812 ms: 1.18x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.2 ms: 1.08x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 98.9 us: 1.04x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 138 us: 1.01x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.51 ms: 1.10x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| django_template | 13.6 ms                                                  | 14.5 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x faster                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.94 ms: 5.27x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.16x faster                                                     |
| mdp                              | 1.09 sec                                                 | 521 ms: 2.10x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 217 ms: 2.06x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 229 ms: 2.00x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.5 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 99.5 ms: 1.73x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.70x faster                                                     |
| deepcopy                         | 161 us                                                   | 97.2 us: 1.66x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.63x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.9 us: 1.54x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.88 us: 1.43x faster                                                    |
| float                            | 37.9 ms                                                  | 26.6 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                    |
| go                               | 70.0 ms                                                  | 52.1 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 249 ms: 1.34x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 41.6 ms: 1.31x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.6 ms: 1.30x faster                                                    |
| raytrace                         | 145 ms                                                   | 113 ms: 1.29x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.26x faster                                                     |
| k_core                           | 1.12 sec                                                 | 894 ms: 1.25x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.2 ms: 1.24x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 114 ms: 1.24x faster                                                     |
| nbody                            | 54.2 ms                                                  | 44.0 ms: 1.23x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.44 ms: 1.20x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 45.7 ms: 1.19x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.3 ms: 1.19x faster                                                    |
| pyflate                          | 216 ms                                                   | 182 ms: 1.19x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 36.6 ms: 1.19x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.16 us: 1.19x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.75 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 43.0 ns: 1.18x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.89 sec: 1.18x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.37 us: 1.18x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.3 ms: 1.18x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 812 ms: 1.18x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 44.3 ms: 1.16x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.0 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.7 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.14x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.72 ms: 1.12x faster                                                    |
| sphinx                           | 434 ms                                                   | 392 ms: 1.11x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 23.0 ms: 1.10x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.51 ms: 1.10x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.3 ms: 1.10x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.5 us: 1.10x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.36 ms: 1.09x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.2 ms: 1.09x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 460 ms: 1.08x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 63.2 ms: 1.08x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| fannkuch                         | 176 ms                                                   | 167 ms: 1.05x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 312 ms: 1.05x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 634 ms: 1.05x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.1 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.7 ms: 1.04x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 98.9 us: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                     |
| json                             | 1.93 ms                                                  | 1.86 ms: 1.04x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 937 ns: 1.03x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 998 ms: 1.02x faster                                                     |
| thrift                           | 322 us                                                   | 315 us: 1.02x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 38.1 ms: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 138 us: 1.01x faster                                                     |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| shortest_path                    | 219 ms                                                   | 221 ms: 1.01x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 424 us: 1.01x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                     |
| connected_components             | 201 ms                                                   | 205 ms: 1.02x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.1 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.5 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.85 ms: 1.09x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.11x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 934 us: 1.13x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 44.9 ms: 1.13x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.39 ms: 1.19x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                    |
| many_optionals                   | 195 us                                                   | 244 us: 1.25x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.5 ms: 2.51x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.17x faster                                                             |

Benchmark hidden because not significant (3): regex_v8, pidigits, mako
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260407-3.15.0a8+-0b20bff/bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.172x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.24x