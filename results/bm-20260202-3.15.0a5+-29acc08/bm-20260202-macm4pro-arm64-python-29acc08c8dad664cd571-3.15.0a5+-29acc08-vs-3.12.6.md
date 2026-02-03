# Results vs. 3.12.6

- fork: python
- ref: 29acc08c8dad664cd571
- machine: darwin-arm64
- commit hash: 29acc08
- commit date: 2026-02-02
- overall geometric mean: 1.194x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 108 ms: 1.06x faster                                                     |
| docutils       | 1.02 sec                                                 | 979 ms: 1.04x faster                                                     |
| html5lib       | 23.0 ms                                                  | 20.8 ms: 1.11x faster                                                    |
| sphinx         | 434 ms                                                   | 380 ms: 1.14x faster                                                     |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 213 ms: 2.33x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 211 ms: 2.12x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 221 ms: 2.07x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 94.5 ms: 1.82x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.1 ms: 1.80x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.73x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 242 ms: 1.40x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.26x faster                                                     |
| async_generators                 | 206 ms                                                   | 167 ms: 1.24x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 38.8 ms: 1.18x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 211 ms: 1.10x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 181 ms: 1.05x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 117 ms: 1.03x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.3 ms: 2.40x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.5 ms: 1.38x faster                                                    |
| nbody          | 54.2 ms                                                  | 43.7 ms: 1.24x faster                                                    |
| pidigits       | 161 ms                                                   | 156 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.21x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 44.5 ms: 1.23x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.3 ms: 1.08x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.64 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.3 ms: 1.38x faster                                                    |
| tomli_loads          | 957 ms                                                   | 818 ms: 1.17x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 59.0 ms: 1.15x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 33.7 ms: 1.15x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 23.8 ms: 1.12x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 94.8 us: 1.09x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.3 us: 1.05x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 136 us: 1.03x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.14x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.25 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.49 ms: 1.10x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.5 ms: 1.06x faster                                                    |
| mako            | 4.77 ms                                                  | 4.59 ms: 1.04x faster                                                    |
| django_template | 13.6 ms                                                  | 14.3 ms: 1.05x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.04x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.83 ms: 5.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 213 ms: 2.33x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 211 ms: 2.12x faster                                                     |
| mdp                              | 1.09 sec                                                 | 526 ms: 2.08x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 221 ms: 2.07x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 94.5 ms: 1.82x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.1 ms: 1.80x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.73x faster                                                     |
| deepcopy                         | 161 us                                                   | 95.2 us: 1.70x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.1 us: 1.65x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 6.91 us: 1.42x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 242 ms: 1.40x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.3 ms: 1.38x faster                                                    |
| float                            | 37.9 ms                                                  | 27.5 ms: 1.38x faster                                                    |
| go                               | 70.0 ms                                                  | 51.4 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 39.5 ns: 1.29x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.26x faster                                                     |
| k_core                           | 1.12 sec                                                 | 897 ms: 1.25x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.0 ms: 1.25x faster                                                    |
| nbody                            | 54.2 ms                                                  | 43.7 ms: 1.24x faster                                                    |
| async_generators                 | 206 ms                                                   | 167 ms: 1.24x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 44.0 ms: 1.23x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.8 ms: 1.23x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 44.5 ms: 1.23x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.41 ms: 1.22x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.15 us: 1.20x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.8 ms: 1.19x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.37 us: 1.18x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 38.8 ms: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.1 ms: 1.17x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 818 ms: 1.17x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.6 ms: 1.17x faster                                                    |
| pyflate                          | 216 ms                                                   | 186 ms: 1.16x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 21.9 ms: 1.16x faster                                                    |
| pylint                           | 128 ms                                                   | 110 ms: 1.16x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 122 ms: 1.16x faster                                                     |
| richards                         | 22.4 ms                                                  | 19.3 ms: 1.16x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 61.3 us: 1.16x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.1 ms: 1.15x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 44.5 ms: 1.15x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.0 ms: 1.15x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 33.7 ms: 1.15x faster                                                    |
| sphinx                           | 434 ms                                                   | 380 ms: 1.14x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.67 ms: 1.14x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 23.8 ms: 1.12x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 20.8 ms: 1.11x faster                                                    |
| pycparser                        | 497 ms                                                   | 450 ms: 1.11x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.25 ms: 1.11x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.49 ms: 1.10x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.89 ms: 1.10x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 211 ms: 1.10x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 300 ms: 1.09x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 609 ms: 1.09x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 94.8 us: 1.09x faster                                                    |
| thrift                           | 322 us                                                   | 297 us: 1.08x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 92.3 ms: 1.08x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 53.4 ms: 1.08x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 20.5 ms: 1.06x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 36.6 ms: 1.06x faster                                                    |
| 2to3                             | 114 ms                                                   | 108 ms: 1.06x faster                                                     |
| sympy_str                        | 104 ms                                                   | 98.4 ms: 1.06x faster                                                    |
| json                             | 1.93 ms                                                  | 1.83 ms: 1.06x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 181 ms: 1.05x faster                                                     |
| fannkuch                         | 176 ms                                                   | 167 ms: 1.05x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.3 us: 1.05x faster                                                    |
| docutils                         | 1.02 sec                                                 | 979 ms: 1.04x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.59 ms: 1.04x faster                                                    |
| pidigits                         | 161 ms                                                   | 156 ms: 1.04x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 136 us: 1.03x faster                                                     |
| gc_traversal                     | 2.01 ms                                                  | 1.96 ms: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 949 ns: 1.02x faster                                                     |
| meteor_contest                   | 47.7 ms                                                  | 47.1 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.01x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.64 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 221 ms: 1.01x slower                                                     |
| connected_components             | 201 ms                                                   | 205 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 117 ms: 1.03x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.3 ms: 1.05x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 882 us: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.82 ms: 1.08x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 43.2 ms: 1.09x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.25 ms: 1.09x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.3 ms: 1.16x slower                                                    |
| many_optionals                   | 195 us                                                   | 237 us: 1.21x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.3 ms: 2.40x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.19x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260202-3.15.0a5+-29acc08/bm-20260202-macm4pro-arm64-python-29acc08c8dad664cd571-3.15.0a5+-29acc08.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.194x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.23x