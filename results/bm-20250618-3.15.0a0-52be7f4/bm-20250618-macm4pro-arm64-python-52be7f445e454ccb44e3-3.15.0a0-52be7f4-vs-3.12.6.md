# Results vs. 3.12.6

- fork: python
- ref: 52be7f445e454ccb44e3
- machine: darwin-arm64
- commit hash: 52be7f4
- commit date: 2025-06-18
- overall geometric mean: 1.102x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.3 ms: 1.06x slower                                                   |
| sphinx         | 434 ms                                                   | 411 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.90x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 269 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 272 ms: 1.23x faster                                                    |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.5 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 253 ms: 1.19x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.6 ms: 2.76x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.1 ms: 1.26x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.5 ms: 1.14x faster                                                   |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 48.2 ms: 1.13x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.7 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.74 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 45.1 ms: 1.14x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.2 ms: 1.10x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 98.2 us: 1.05x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 65.4 ms: 1.04x faster                                                   |
| tomli_loads          | 957 ms                                                   | 928 ms: 1.03x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.8 us: 1.01x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 4.48 ms: 1.05x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.00 ms: 1.05x faster                                                  |
| mako            | 4.77 ms                                                  | 4.86 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 513 ms: 2.13x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.84 ms: 2.11x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.90x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                   |
| deepcopy                         | 161 us                                                   | 111 us: 1.46x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.29 us: 1.35x faster                                                   |
| float                            | 37.9 ms                                                  | 30.1 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 269 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.6 ms: 1.25x faster                                                   |
| raytrace                         | 145 ms                                                   | 117 ms: 1.23x faster                                                    |
| go                               | 70.0 ms                                                  | 57.0 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 272 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.8 ms: 1.22x faster                                                   |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.0 ms: 1.21x faster                                                   |
| k_core                           | 1.12 sec                                                 | 946 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| nbody                            | 54.2 ms                                                  | 47.5 ms: 1.14x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.1 ms: 1.14x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.4 us: 1.14x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.52 ms: 1.14x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.2 ms: 1.13x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.4 ms: 1.13x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.7 ms: 1.12x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.85 ms: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 115 ms: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.0 ms: 1.11x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.2 ms: 1.10x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.77 ms: 1.10x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.48 ms: 1.07x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.5 ms: 1.07x faster                                                   |
| thrift                           | 322 us                                                   | 302 us: 1.06x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 411 ms: 1.05x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 48.7 ms: 1.05x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.00 ms: 1.05x faster                                                  |
| unpickle_pure_python             | 103 us                                                   | 98.2 us: 1.05x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.4 ms: 1.05x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 65.4 ms: 1.04x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 928 ms: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.2 ms: 1.02x faster                                                   |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 97.7 ms: 1.02x faster                                                   |
| richards                         | 22.4 ms                                                  | 22.0 ms: 1.02x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 38.3 ms: 1.01x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 955 ns: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.77 us: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.8 us: 1.01x faster                                                   |
| shortest_path                    | 219 ms                                                   | 220 ms: 1.00x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.00x slower                                                    |
| connected_components             | 201 ms                                                   | 202 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.3 ms: 1.01x slower                                                   |
| 2to3                             | 114 ms                                                   | 116 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.02x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.74 ms: 1.02x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.86 ms: 1.02x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 432 us: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.48 ms: 1.05x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.3 ms: 1.06x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.06x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.13 ms: 1.06x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 721 ms: 1.08x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 356 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.9 ms: 1.13x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.98 ms: 1.14x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.14x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 967 us: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 253 ms: 1.19x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.1 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 252 us: 1.29x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.6 ms: 2.76x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 197 ns: 3.86x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (5): richards_super, pycparser, fannkuch, logging_simple, genshi_xml
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250618-3.15.0a0-52be7f4/bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.102x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x