# Results vs. 3.12.6

- fork: python
- ref: dd88e77fad887aaf00ea
- machine: darwin-arm64
- commit hash: dd88e77
- commit date: 2026-04-10
- overall geometric mean: 1.181x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                     |
| docutils       | 1.02 sec                                                 | 987 ms: 1.04x faster                                                     |
| html5lib       | 23.0 ms                                                  | 20.8 ms: 1.11x faster                                                    |
| sphinx         | 434 ms                                                   | 388 ms: 1.12x faster                                                     |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 214 ms: 2.32x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 220 ms: 2.18x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 213 ms: 2.09x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 227 ms: 2.02x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 98.3 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 98.3 ms: 1.75x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 133 ms: 1.67x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 244 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.27x faster                                                     |
| async_generators                 | 206 ms                                                   | 174 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 39.9 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 213 ms: 1.08x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.04x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 232 ms: 1.09x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.4 ms: 2.50x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.5 ms: 1.43x faster                                                    |
| nbody          | 54.2 ms                                                  | 43.6 ms: 1.24x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.22x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 44.7 ms: 1.22x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.3 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.46 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| tomli_loads          | 957 ms                                                   | 801 ms: 1.20x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.66 ms: 1.16x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.9 ms: 1.11x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 62.1 ms: 1.09x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 95.3 us: 1.08x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.4 us: 1.04x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 138 us: 1.01x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.12x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.67 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.45 ms: 1.11x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| mako            | 4.77 ms                                                  | 4.70 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 14.5 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.85 ms: 5.40x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 214 ms: 2.32x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 220 ms: 2.18x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 213 ms: 2.09x faster                                                     |
| mdp                              | 1.09 sec                                                 | 525 ms: 2.08x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 227 ms: 2.02x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 98.3 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 98.3 ms: 1.75x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 133 ms: 1.67x faster                                                     |
| deepcopy                         | 161 us                                                   | 97.6 us: 1.66x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.4 us: 1.61x faster                                                    |
| float                            | 37.9 ms                                                  | 26.5 ms: 1.43x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.93 us: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 244 ms: 1.39x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.06 us: 1.38x faster                                                    |
| go                               | 70.0 ms                                                  | 51.2 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 41.2 ms: 1.32x faster                                                    |
| raytrace                         | 145 ms                                                   | 112 ms: 1.29x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.27x faster                                                     |
| k_core                           | 1.12 sec                                                 | 894 ms: 1.25x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.8 ns: 1.25x faster                                                    |
| nbody                            | 54.2 ms                                                  | 43.6 ms: 1.24x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.6 ms: 1.23x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.41 ms: 1.22x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 44.7 ms: 1.22x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.1 ms: 1.21x faster                                                    |
| chaos                            | 28.9 ms                                                  | 23.9 ms: 1.21x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 36.1 ms: 1.20x faster                                                    |
| pyflate                          | 216 ms                                                   | 181 ms: 1.20x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 801 ms: 1.20x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.15 us: 1.19x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.36 us: 1.19x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 119 ms: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 174 ms: 1.18x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.90 sec: 1.18x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.17x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.6 ms: 1.17x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.66 ms: 1.16x faster                                                    |
| pylint                           | 128 ms                                                   | 112 ms: 1.15x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 39.9 ms: 1.14x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 45.2 ms: 1.14x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.70 ms: 1.13x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.7 ms: 1.12x faster                                                    |
| sphinx                           | 434 ms                                                   | 388 ms: 1.12x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 34.9 ms: 1.11x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.7 us: 1.11x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.2 ms: 1.11x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.45 ms: 1.11x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 20.8 ms: 1.11x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.88 ms: 1.10x faster                                                    |
| pycparser                        | 497 ms                                                   | 454 ms: 1.10x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 62.1 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.35 ms: 1.09x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 213 ms: 1.08x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 303 ms: 1.08x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 95.3 us: 1.08x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 618 ms: 1.08x faster                                                     |
| fannkuch                         | 176 ms                                                   | 166 ms: 1.06x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 94.3 ms: 1.06x faster                                                    |
| json                             | 1.93 ms                                                  | 1.84 ms: 1.05x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 54.8 ms: 1.05x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.7 ms: 1.05x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 925 ns: 1.04x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.4 us: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.04x faster                                                     |
| docutils                         | 1.02 sec                                                 | 987 ms: 1.04x faster                                                     |
| thrift                           | 322 us                                                   | 313 us: 1.03x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.8 ms: 1.03x faster                                                    |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.70 ms: 1.02x faster                                                    |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.46 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 138 us: 1.01x faster                                                     |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 427 us: 1.02x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 48.8 ms: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 208 ms: 1.04x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.5 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.67 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.85 ms: 1.09x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 232 ms: 1.09x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 934 us: 1.13x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.1 ms: 1.14x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.38 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.9 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 242 us: 1.24x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.4 ms: 2.50x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.18x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260410-3.15.0a8+-dd88e77/bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.181x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.24x