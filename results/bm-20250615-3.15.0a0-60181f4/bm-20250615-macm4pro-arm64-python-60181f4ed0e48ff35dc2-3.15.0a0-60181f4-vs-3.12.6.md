# Results vs. 3.12.6

- fork: python
- ref: 60181f4ed0e48ff35dc2
- machine: darwin-arm64
- commit hash: 60181f4
- commit date: 2025-06-15
- overall geometric mean: 1.108x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 114 ms: 1.00x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.8 ms: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 255 ms: 1.80x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.62x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 268 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 269 ms: 1.24x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.4 ms: 1.08x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.0 ms: 2.74x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.0 ms: 1.26x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.4 ms: 1.14x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.8 ms: 1.14x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.79 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.6 ms: 1.16x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.2 ms: 1.10x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 62.6 ms: 1.09x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                   |
| tomli_loads          | 957 ms                                                   | 901 ms: 1.06x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.6 us: 1.06x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 4.44 ms: 1.04x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.67 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.86 ms: 1.06x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                   |
| mako            | 4.77 ms                                                  | 4.81 ms: 1.01x slower                                                   |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.71 ms: 2.14x faster                                                   |
| mdp                              | 1.09 sec                                                 | 513 ms: 2.13x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 255 ms: 1.80x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.62x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.3 us: 1.48x faster                                                   |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.39 us: 1.33x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                   |
| float                            | 37.9 ms                                                  | 30.0 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 268 ms: 1.26x faster                                                    |
| go                               | 70.0 ms                                                  | 55.6 ms: 1.26x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.5 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 269 ms: 1.24x faster                                                    |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.8 ms: 1.22x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 45.5 ms: 1.19x faster                                                   |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.8 ms: 1.19x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| k_core                           | 1.12 sec                                                 | 950 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.6 ms: 1.16x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 61.7 us: 1.15x faster                                                   |
| nbody                            | 54.2 ms                                                  | 47.4 ms: 1.14x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 47.8 ms: 1.14x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.1 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| deltablue                        | 1.73 ms                                                  | 1.52 ms: 1.14x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.84 ms: 1.13x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                    |
| pyflate                          | 216 ms                                                   | 193 ms: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.74 ms: 1.11x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.1 ms: 1.11x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.2 ms: 1.10x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.2 ms: 1.10x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 62.6 ms: 1.09x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.45 ms: 1.08x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.4 ms: 1.08x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.0 ms: 1.07x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.86 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 901 ms: 1.06x faster                                                    |
| thrift                           | 322 us                                                   | 304 us: 1.06x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 97.6 us: 1.06x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.0 ms: 1.05x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.3 ms: 1.05x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.6 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.6 ms: 1.03x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.0 ms: 1.03x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.74 us: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                   |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                   |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.55 us: 1.01x faster                                                   |
| 2to3                             | 114 ms                                                   | 114 ms: 1.00x slower                                                    |
| shortest_path                    | 219 ms                                                   | 220 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.81 ms: 1.01x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 48.2 ms: 1.01x slower                                                   |
| connected_components             | 201 ms                                                   | 203 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.79 ms: 1.02x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| bench_thread_pool                | 419 us                                                   | 432 us: 1.03x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.8 ms: 1.03x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.44 ms: 1.04x slower                                                   |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.12 ms: 1.05x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 707 ms: 1.06x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 349 ms: 1.06x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.67 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.7 ms: 1.13x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.13x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 949 us: 1.14x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.9 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 247 us: 1.27x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.0 ms: 2.74x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 196 ns: 3.86x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (4): sqlite_synth, pycparser, json_loads, regex_dna
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250615-3.15.0a0-60181f4/bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.108x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x