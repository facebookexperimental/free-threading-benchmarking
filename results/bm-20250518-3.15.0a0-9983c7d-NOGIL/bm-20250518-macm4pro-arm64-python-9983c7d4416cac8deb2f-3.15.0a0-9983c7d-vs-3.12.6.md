# Results vs. 3.12.6

- fork: python
- ref: 9983c7d4416cac8deb2f
- machine: darwin-arm64
- commit hash: 9983c7d
- commit date: 2025-05-18
- overall geometric mean: 1.083x faster
- HPT reliability: 96.75%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 25.8 ms: 1.12x slower                                                   |
| sphinx         | 434 ms                                                   | 421 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.2 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 50.6 ms: 1.11x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| nbody          | 54.2 ms                                                  | 56.2 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.29 ms: 1.03x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.1 ms: 1.32x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.5 ms: 1.14x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.7 ms: 1.03x faster                                                   |
| tomli_loads          | 957 ms                                                   | 984 ms: 1.03x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.5 ms: 1.03x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 155 us: 1.11x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.84 ms: 1.14x slower                                                   |
| json_loads           | 10.9 us                                                  | 12.6 us: 1.16x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.43 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.87 ms: 1.20x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                   |
| mako            | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                   |
| django_template | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 779 us: 2.58x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.92 ms: 2.09x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 87.2 ms: 1.98x faster                                                   |
| mdp                              | 1.09 sec                                                 | 577 ms: 1.89x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 492 us: 1.69x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                    |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.1 ms: 1.32x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                   |
| deepcopy                         | 161 us                                                   | 125 us: 1.30x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.2 us: 1.29x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 823 ns: 1.18x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.7 ms: 1.17x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.28 us: 1.15x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 59.5 ms: 1.14x faster                                                   |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.13x faster                                                  |
| comprehensions                   | 9.84 us                                                  | 8.72 us: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 993 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| go                               | 70.0 ms                                                  | 63.5 ms: 1.10x faster                                                   |
| raytrace                         | 145 ms                                                   | 133 ms: 1.09x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 56.5 ms: 1.08x faster                                                   |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                    |
| pyflate                          | 216 ms                                                   | 201 ms: 1.08x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.07x faster                                                   |
| pycparser                        | 497 ms                                                   | 474 ms: 1.05x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.6 ms: 1.05x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 52.5 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.29 ms: 1.03x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.7 ms: 1.03x faster                                                   |
| sphinx                           | 434 ms                                                   | 421 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 141 ms: 1.00x faster                                                    |
| chaos                            | 28.9 ms                                                  | 29.7 ms: 1.03x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 984 ms: 1.03x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.5 ms: 1.03x slower                                                   |
| fannkuch                         | 176 ms                                                   | 182 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.2 ms: 1.04x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                   |
| thrift                           | 322 us                                                   | 336 us: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.17 ms: 1.05x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.9 ms: 1.05x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.7 ms: 1.05x slower                                                   |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                    |
| shortest_path                    | 219 ms                                                   | 231 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 75.8 us: 1.07x slower                                                   |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 355 ms: 1.08x slower                                                    |
| json                             | 1.93 ms                                                  | 2.09 ms: 1.08x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.4 ms: 1.09x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 725 ms: 1.09x slower                                                    |
| connected_components             | 201 ms                                                   | 219 ms: 1.09x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.9 ms: 1.10x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.8 ms: 1.10x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.84 us: 1.11x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 50.6 ms: 1.11x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 155 us: 1.11x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.14 us: 1.12x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 25.8 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.7 ms: 1.13x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.84 ms: 1.14x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 55.3 ms: 1.16x slower                                                   |
| json_loads                       | 10.9 us                                                  | 12.6 us: 1.16x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.43 ms: 1.18x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.87 ms: 1.20x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 63.4 ms: 1.24x slower                                                   |
| django_template                  | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.36 ms: 1.29x slower                                                   |
| many_optionals                   | 195 us                                                   | 259 us: 1.33x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 583 us: 1.39x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.0 ms: 1.49x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 214 ns: 4.20x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                            |

Benchmark hidden because not significant (2): sympy_integrate, pidigits
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250518-3.15.0a0-9983c7d-NOGIL/bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.083x faster

# HPT report

- Reliability score: 96.75% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x