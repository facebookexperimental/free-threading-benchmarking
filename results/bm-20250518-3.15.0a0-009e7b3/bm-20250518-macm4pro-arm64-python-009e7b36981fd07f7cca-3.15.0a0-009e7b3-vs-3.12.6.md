# Results vs. 3.12.6

- fork: python
- ref: 009e7b36981fd07f7cca
- machine: darwin-arm64
- commit hash: 009e7b3
- commit date: 2025-05-18
- overall geometric mean: 1.100x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 26.2 ms: 1.14x slower                                                   |
| sphinx         | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 255 ms: 1.80x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.65x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.52x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.2 ms: 1.08x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.3 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| nbody          | 54.2 ms                                                  | 49.6 ms: 1.09x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 48.6 ms: 1.12x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 102 ms: 1.02x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 9.99 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.7 ms: 1.18x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 62.8 ms: 1.08x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.5 ms: 1.05x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 99.0 us: 1.04x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.7 us: 1.07x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.61 ms: 1.08x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.54 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.12 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.94 ms: 1.06x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.7 ms: 1.01x faster                                                   |
| mako            | 4.77 ms                                                  | 4.80 ms: 1.00x slower                                                   |
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.74 ms: 2.13x faster                                                   |
| mdp                              | 1.09 sec                                                 | 524 ms: 2.08x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 255 ms: 1.80x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.65x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.52x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.4 us: 1.47x faster                                                   |
| deepcopy                         | 161 us                                                   | 111 us: 1.45x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| float                            | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.3 ms: 1.27x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.79 us: 1.26x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| go                               | 70.0 ms                                                  | 57.0 ms: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 119 ms: 1.22x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.9 ms: 1.19x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.7 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 949 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 52.4 ms: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.15x faster                                                  |
| deltablue                        | 1.73 ms                                                  | 1.50 ms: 1.15x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 47.7 ms: 1.14x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.2 ms: 1.14x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.6 ms: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.77 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.4 ms: 1.10x faster                                                   |
| nbody                            | 54.2 ms                                                  | 49.6 ms: 1.09x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.7 ms: 1.08x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 62.8 ms: 1.08x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.2 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.47 ms: 1.07x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 66.2 us: 1.07x faster                                                   |
| thrift                           | 322 us                                                   | 303 us: 1.06x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.94 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.5 ms: 1.05x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.5 ms: 1.05x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 49.0 ms: 1.05x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 136 ms: 1.04x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.99 ms: 1.04x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 99.0 us: 1.04x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.6 ms: 1.03x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 318 ms: 1.03x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 645 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.1 ms: 1.03x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.9 ms: 1.02x faster                                                   |
| shortest_path                    | 219 ms                                                   | 214 ms: 1.02x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.1 ms: 1.02x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 950 ns: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                    |
| connected_components             | 201 ms                                                   | 198 ms: 1.01x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.77 us: 1.01x faster                                                   |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.01x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.55 us: 1.01x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.7 ms: 1.01x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.80 ms: 1.00x slower                                                   |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                   |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                    |
| regex_dna                        | 99.6 ms                                                  | 102 ms: 1.02x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.03x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 436 us: 1.04x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.99 ms: 1.04x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 50.8 ms: 1.06x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.54 ms: 1.07x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.12 ms: 1.07x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.7 us: 1.07x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.61 ms: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.0 ms: 1.11x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 929 us: 1.12x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 26.2 ms: 1.14x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.06 ms: 1.17x slower                                                   |
| coverage                         | 26.9 ms                                                  | 33.0 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 248 us: 1.27x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.3 ms: 2.72x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 195 ns: 3.83x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (2): pycparser, tomli_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x