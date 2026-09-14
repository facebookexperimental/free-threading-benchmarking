# Results vs. 3.12.6

- fork: python
- ref: fd0970c0ab7eb8c685ef
- machine: darwin-arm64
- commit hash: fd0970c
- commit date: 2026-09-13
- overall geometric mean: 1.138x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.04x slower                                                    |
| docutils       | 1.02 sec                                                 | 945 ms: 1.08x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.4 ms: 1.08x faster                                                   |
| sphinx         | 434 ms                                                   | 399 ms: 1.09x faster                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 328 ms: 1.46x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 340 ms: 1.46x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.35 ms: 1.45x faster                                                   |
| async_generators                 | 206 ms                                                   | 145 ms: 1.43x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.37x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 341 ms: 1.35x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 335 ms: 1.33x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.33x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 137 ms: 1.30x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 184 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 286 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 293 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 135 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 250 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 266 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 154 ms: 1.37x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 65.2 ms: 1.43x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 103 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.6 ms: 1.33x faster                                                   |
| nbody          | 54.2 ms                                                  | 43.9 ms: 1.23x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.16x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.4 ms: 1.08x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.34 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.6 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 794 ms: 1.21x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.54 ms: 1.20x faster                                                   |
| xml_etree_iterparse  | 51.6 ms                                                  | 43.7 ms: 1.18x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 94.4 us: 1.09x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.8 ms: 1.09x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.00x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (2): json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.29 ms: 1.16x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.76 ms: 1.18x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.17x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.55 ms: 1.05x faster                                                   |
| django_template | 13.6 ms                                                  | 14.9 ms: 1.10x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.09 ms: 5.08x faster                                                   |
| pylint                           | 128 ms                                                   | 56.7 ms: 2.26x faster                                                   |
| mdp                              | 1.09 sec                                                 | 509 ms: 2.15x faster                                                    |
| deepcopy                         | 161 us                                                   | 96.6 us: 1.67x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.57x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.60 us: 1.49x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 328 ms: 1.46x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 340 ms: 1.46x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.35 ms: 1.45x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 49.0 us: 1.45x faster                                                   |
| async_generators                 | 206 ms                                                   | 145 ms: 1.43x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.41x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.37x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 341 ms: 1.35x faster                                                    |
| go                               | 70.0 ms                                                  | 52.2 ms: 1.34x faster                                                   |
| async_tree_eager_io_tg           | 446 ms                                                   | 335 ms: 1.33x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.33x faster                                                    |
| float                            | 37.9 ms                                                  | 28.6 ms: 1.33x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 137 ms: 1.30x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.1 ms: 1.28x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 42.8 ms: 1.27x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                   |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 34.6 ms: 1.26x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 40.5 ns: 1.26x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 48.8 ms: 1.25x faster                                                   |
| nbody                            | 54.2 ms                                                  | 43.9 ms: 1.23x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 115 ms: 1.23x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 184 ms: 1.21x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 794 ms: 1.21x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.54 ms: 1.20x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.15 us: 1.19x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                   |
| pyflate                          | 216 ms                                                   | 181 ms: 1.19x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.36 us: 1.19x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.7 ms: 1.18x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.77 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 286 ms: 1.17x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.6 ms: 1.17x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 293 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.64 ms: 1.15x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.1 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| k_core                           | 1.12 sec                                                 | 983 ms: 1.14x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.0 ms: 1.12x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 22.8 ms: 1.11x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 298 ms: 1.10x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 94.4 us: 1.09x faster                                                   |
| fannkuch                         | 176 ms                                                   | 161 ms: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 399 ms: 1.09x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.8 ms: 1.09x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 613 ms: 1.08x faster                                                    |
| docutils                         | 1.02 sec                                                 | 945 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.43 ms: 1.08x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 92.4 ms: 1.08x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 21.4 ms: 1.08x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.5 ms: 1.06x faster                                                   |
| sympy_str                        | 104 ms                                                   | 98.9 ms: 1.05x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.55 ms: 1.05x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.2 ms: 1.04x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 928 ns: 1.04x faster                                                    |
| thrift                           | 322 us                                                   | 312 us: 1.03x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.34 ms: 1.03x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 1.96 ms: 1.03x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 53.6 ms: 1.02x faster                                                   |
| pycparser                        | 497 ms                                                   | 490 ms: 1.02x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 819 us: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                   |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.00x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 135 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.8 ms: 1.02x slower                                                   |
| connected_components             | 201 ms                                                   | 205 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 119 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 250 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.85 ms: 1.09x slower                                                   |
| django_template                  | 13.6 ms                                                  | 14.9 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.7 ms: 1.15x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.29 ms: 1.16x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.76 ms: 1.18x slower                                                   |
| many_optionals                   | 195 us                                                   | 244 us: 1.25x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 266 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 154 ms: 1.37x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 65.2 ms: 1.43x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 103 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmark hidden because not significant (4): json_loads, bench_thread_pool, asyncio_websockets, xml_etree_parse
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260913-3.16.0a0-fd0970c/bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.138x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.22x