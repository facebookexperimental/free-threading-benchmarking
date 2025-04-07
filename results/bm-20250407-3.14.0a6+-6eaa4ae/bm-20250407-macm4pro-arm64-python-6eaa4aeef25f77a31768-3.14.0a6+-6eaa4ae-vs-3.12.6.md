# Results vs. 3.12.6

- fork: python
- ref: 6eaa4aeef25f77a31768
- machine: darwin-arm64
- commit hash: 6eaa4ae
- commit date: 2025-04-07
- overall geometric mean: 1.109x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.03x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.00x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                    |
| sphinx         | 434 ms                                                   | 407 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 248 ms: 1.93x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 255 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.65x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.52x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_generators                 | 206 ms                                                   | 170 ms: 1.21x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 42.7 ms: 1.07x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.1 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.4 ms: 1.29x faster                                                    |
| nbody          | 54.2 ms                                                  | 50.4 ms: 1.08x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.12x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 48.3 ms: 1.13x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.8 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.90 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.0 ms: 1.20x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.0 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                    |
| tomli_loads          | 957 ms                                                   | 927 ms: 1.03x faster                                                     |
| unpickle_pure_python | 103 us                                                   | 102 us: 1.01x faster                                                     |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.03x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 4.98 ms: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.95 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.72 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.5 ms: 1.01x faster                                                    |
| mako            | 4.77 ms                                                  | 4.83 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.60 ms: 2.42x faster                                                    |
| mdp                              | 1.09 sec                                                 | 521 ms: 2.10x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 248 ms: 1.93x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 255 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.65x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.52x faster                                                     |
| deepcopy                         | 161 us                                                   | 111 us: 1.46x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 7.62 us: 1.29x faster                                                    |
| float                            | 37.9 ms                                                  | 29.4 ms: 1.29x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.5 ns: 1.23x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.0 ms: 1.22x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.5 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 170 ms: 1.21x faster                                                     |
| go                               | 70.0 ms                                                  | 58.0 ms: 1.21x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.0 ms: 1.20x faster                                                    |
| raytrace                         | 145 ms                                                   | 121 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 51.5 ms: 1.18x faster                                                    |
| k_core                           | 1.12 sec                                                 | 946 ms: 1.18x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 47.6 ms: 1.14x faster                                                    |
| pylint                           | 128 ms                                                   | 112 ms: 1.14x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 48.3 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.54 ms: 1.12x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.2 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 196 ms: 1.11x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 64.8 us: 1.10x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.5 ms: 1.09x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 47.4 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.43 ms: 1.08x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.0 ms: 1.08x faster                                                    |
| nbody                            | 54.2 ms                                                  | 50.4 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.9 ms: 1.08x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.83 ms: 1.08x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.40 us: 1.07x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.62 us: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 42.7 ms: 1.07x faster                                                    |
| sphinx                           | 434 ms                                                   | 407 ms: 1.06x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 44.6 ms: 1.05x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.6 ms: 1.05x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 927 ns: 1.04x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.99 ms: 1.04x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.4 ms: 1.04x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                    |
| 2to3                             | 114 ms                                                   | 110 ms: 1.03x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 927 ms: 1.03x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 96.8 ms: 1.03x faster                                                    |
| pycparser                        | 497 ms                                                   | 487 ms: 1.02x faster                                                     |
| pidigits                         | 161 ms                                                   | 159 ms: 1.02x faster                                                     |
| gc_traversal                     | 2.01 ms                                                  | 1.98 ms: 1.02x faster                                                    |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                    |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.01x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.5 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 102 us: 1.01x faster                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 39.6 ms: 1.00x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 167 ms: 1.00x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.00x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 330 ms: 1.01x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.83 ms: 1.01x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.1 ms: 1.03x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.90 ms: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.03x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 434 us: 1.04x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.37 ms: 1.04x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 862 us: 1.04x slower                                                     |
| fannkuch                         | 176 ms                                                   | 183 ms: 1.04x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.95 ms: 1.12x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.1 ms: 1.16x slower                                                    |
| many_optionals                   | 195 us                                                   | 228 us: 1.17x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 4.98 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.72 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.1 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (4): richards_super, connected_components, richards, pprint_pformat
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250407-3.14.0a6+-6eaa4ae/bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.109x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.13x