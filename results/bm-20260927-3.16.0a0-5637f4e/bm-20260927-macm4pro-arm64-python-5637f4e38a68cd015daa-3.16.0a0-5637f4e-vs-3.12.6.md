# Results vs. 3.12.6

- fork: python
- ref: 5637f4e38a68cd015daa
- machine: darwin-arm64
- commit hash: 5637f4e
- commit date: 2026-09-27
- overall geometric mean: 1.132x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| docutils       | 1.02 sec                                                 | 956 ms: 1.07x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                   |
| sphinx         | 434 ms                                                   | 400 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 329 ms: 1.46x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 343 ms: 1.45x faster                                                    |
| async_generators                 | 206 ms                                                   | 144 ms: 1.43x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.52 ms: 1.43x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.38x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.33x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 345 ms: 1.33x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 136 ms: 1.31x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 342 ms: 1.30x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 183 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 287 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 293 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 134 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 251 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 266 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 154 ms: 1.37x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 65.1 ms: 1.43x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 104 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                   |
| nbody          | 54.2 ms                                                  | 43.0 ms: 1.26x faster                                                   |
| pidigits       | 161 ms                                                   | 167 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.17x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.33 ms: 1.25x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 91.9 ms: 1.08x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.29 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.3 ms: 1.22x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.56 ms: 1.20x faster                                                   |
| tomli_loads          | 957 ms                                                   | 817 ms: 1.17x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.8 ms: 1.09x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.1 ms: 1.07x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 64.0 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.02x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.19 ms: 1.15x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.70 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.16x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.58 ms: 1.04x faster                                                   |
| django_template | 13.6 ms                                                  | 14.8 ms: 1.08x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.11 ms: 5.05x faster                                                   |
| pylint                           | 128 ms                                                   | 56.2 ms: 2.28x faster                                                   |
| mdp                              | 1.09 sec                                                 | 512 ms: 2.13x faster                                                    |
| deepcopy                         | 161 us                                                   | 95.8 us: 1.69x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 11.9 us: 1.54x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.69 us: 1.47x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 329 ms: 1.46x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 48.9 us: 1.45x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 343 ms: 1.45x faster                                                    |
| async_generators                 | 206 ms                                                   | 144 ms: 1.43x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.52 ms: 1.43x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.41x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.38x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.33x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 345 ms: 1.33x faster                                                    |
| go                               | 70.0 ms                                                  | 52.6 ms: 1.33x faster                                                   |
| float                            | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 136 ms: 1.31x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 342 ms: 1.30x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 42.7 ms: 1.27x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.4 ms: 1.26x faster                                                   |
| nbody                            | 54.2 ms                                                  | 43.0 ms: 1.26x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.33 ms: 1.25x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 35.0 ms: 1.24x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 49.4 ms: 1.24x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.7 ns: 1.22x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 183 ms: 1.22x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.3 ms: 1.22x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 117 ms: 1.21x faster                                                    |
| raytrace                         | 145 ms                                                   | 121 ms: 1.20x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.56 ms: 1.20x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.18 us: 1.18x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 817 ms: 1.17x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 287 ms: 1.16x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.78 ms: 1.16x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.41 us: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 293 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| k_core                           | 1.12 sec                                                 | 978 ms: 1.14x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.4 ms: 1.13x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.6 ms: 1.13x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.69 ms: 1.13x faster                                                   |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.3 ms: 1.11x faster                                                   |
| fannkuch                         | 176 ms                                                   | 159 ms: 1.11x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.0 ms: 1.10x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 301 ms: 1.09x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.8 ms: 1.09x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 91.9 ms: 1.08x faster                                                   |
| sphinx                           | 434 ms                                                   | 400 ms: 1.08x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 618 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.46 ms: 1.07x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                   |
| docutils                         | 1.02 sec                                                 | 956 ms: 1.07x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.1 ms: 1.07x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.2 ms: 1.06x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 64.0 ms: 1.06x faster                                                   |
| sympy_str                        | 104 ms                                                   | 98.9 ms: 1.05x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.58 ms: 1.04x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.3 ms: 1.04x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 929 ns: 1.04x faster                                                    |
| thrift                           | 322 us                                                   | 310 us: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.29 ms: 1.03x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 1.95 ms: 1.03x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.02x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.2 ms: 1.02x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                   |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                   |
| pycparser                        | 497 ms                                                   | 491 ms: 1.01x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 836 us: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 221 ms: 1.01x slower                                                    |
| connected_components             | 201 ms                                                   | 204 ms: 1.02x slower                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 134 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.9 ms: 1.02x slower                                                   |
| pidigits                         | 161 ms                                                   | 167 ms: 1.03x slower                                                    |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.8 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 251 ms: 1.09x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.87 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.3 ms: 1.14x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.19 ms: 1.15x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.70 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 266 ms: 1.25x slower                                                    |
| many_optionals                   | 195 us                                                   | 245 us: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 154 ms: 1.37x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 65.1 ms: 1.43x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 104 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                            |

Benchmark hidden because not significant (3): asyncio_websockets, regex_compile, bench_thread_pool
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260927-3.16.0a0-5637f4e/bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.132x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.22x