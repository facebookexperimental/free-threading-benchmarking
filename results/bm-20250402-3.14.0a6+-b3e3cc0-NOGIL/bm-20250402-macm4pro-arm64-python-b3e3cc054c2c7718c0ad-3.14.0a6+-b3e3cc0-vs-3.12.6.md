# Results vs. 3.12.6

- fork: python
- ref: b3e3cc054c2c7718c0ad
- machine: darwin-arm64
- commit hash: b3e3cc0
- commit date: 2025-04-02
- overall geometric mean: 1.085x faster
- HPT reliability: 92.24%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 23.6 ms: 1.03x slower                                                    |
| sphinx         | 434 ms                                                   | 425 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 200 ms: 2.39x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 210 ms: 2.36x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 199 ms: 2.24x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 214 ms: 2.14x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 88.2 ms: 1.95x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 126 ms: 1.83x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 133 ms: 1.67x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.29x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                     |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 114 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 51.2 ms: 1.12x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.2 ms: 2.46x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.34x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 53.8 ms: 1.01x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 101 ms: 1.02x slower                                                     |
| regex_v8       | 9.59 ms                                                  | 10.00 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 36.7 ms: 1.40x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.1 ms: 1.21x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.9 ms: 1.00x slower                                                    |
| tomli_loads          | 957 ms                                                   | 976 ms: 1.02x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                     |
| json_loads           | 10.9 us                                                  | 12.0 us: 1.10x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.06 ms: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.53 ms: 1.19x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.58 ms: 1.33x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.26x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.09x slower                                                    |
| mako            | 4.77 ms                                                  | 5.58 ms: 1.17x slower                                                    |
| django_template | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 758 us: 2.65x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 200 ms: 2.39x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 210 ms: 2.36x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 8.90 ms: 2.33x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 199 ms: 2.24x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 214 ms: 2.14x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 88.2 ms: 1.95x faster                                                    |
| mdp                              | 1.09 sec                                                 | 571 ms: 1.91x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 126 ms: 1.83x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 459 us: 1.81x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 133 ms: 1.67x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.7 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                     |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.34x faster                                                    |
| deepcopy                         | 161 us                                                   | 125 us: 1.29x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.29x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.5 us: 1.26x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 56.1 ms: 1.21x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 817 ns: 1.18x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                     |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| k_core                           | 1.12 sec                                                 | 981 ms: 1.14x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.29 us: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.74 us: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| go                               | 70.0 ms                                                  | 63.5 ms: 1.10x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.4 ms: 1.10x faster                                                    |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                     |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                     |
| pylint                           | 128 ms                                                   | 120 ms: 1.07x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 51.3 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                    |
| pycparser                        | 497 ms                                                   | 473 ms: 1.05x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.05x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 49.2 ns: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 42.5 ms: 1.02x faster                                                    |
| sphinx                           | 434 ms                                                   | 425 ms: 1.02x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 53.8 ms: 1.01x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 141 ms: 1.01x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 26.9 ms: 1.00x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 114 ms: 1.01x slower                                                     |
| logging_simple                   | 2.57 us                                                  | 2.60 us: 1.01x slower                                                    |
| regex_dna                        | 99.6 ms                                                  | 101 ms: 1.02x slower                                                     |
| tomli_loads                      | 957 ms                                                   | 976 ms: 1.02x slower                                                     |
| chaos                            | 28.9 ms                                                  | 29.5 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.22 ms: 1.03x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.87 us: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.13 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.9 us: 1.03x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.6 ms: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.4 ms: 1.04x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.00 ms: 1.04x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.18 ms: 1.05x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                     |
| shortest_path                    | 219 ms                                                   | 231 ms: 1.05x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 42.1 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 41.4 ms: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 54.9 ms: 1.07x slower                                                    |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.08x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 62.3 ms: 1.08x slower                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 50.8 ms: 1.09x slower                                                    |
| connected_components             | 201 ms                                                   | 219 ms: 1.09x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.09x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                     |
| fannkuch                         | 176 ms                                                   | 193 ms: 1.10x slower                                                     |
| json_loads                       | 10.9 us                                                  | 12.0 us: 1.10x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.8 ms: 1.10x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 28.3 ms: 1.11x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.77 ms: 1.12x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 51.2 ms: 1.12x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 369 ms: 1.12x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 752 ms: 1.13x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 191 ms: 1.15x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.58 ms: 1.17x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.06 ms: 1.19x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.53 ms: 1.19x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 57.1 ms: 1.20x slower                                                    |
| django_template                  | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                    |
| many_optionals                   | 195 us                                                   | 246 us: 1.26x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.41 ms: 1.30x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.58 ms: 1.33x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 578 us: 1.38x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.8 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.2 ms: 2.46x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (1): nbody
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250402-3.14.0a6+-b3e3cc0-NOGIL/bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.085x faster

# HPT report

- Reliability score: 92.24% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.22x