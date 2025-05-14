# Results vs. 3.12.6

- fork: python
- ref: 9ad0c7b0f14c5fcda6bf
- machine: darwin-arm64
- commit hash: 9ad0c7b
- commit date: 2025-05-13
- overall geometric mean: 1.075x faster
- HPT reliability: 86.74%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| html5lib       | 23.0 ms                                                  | 26.3 ms: 1.14x slower                                                   |
| sphinx         | 434 ms                                                   | 425 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.05x slower                                                            |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.39x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.27x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 88.5 ms: 1.94x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 132 ms: 1.69x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 238 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 230 ms: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 50.9 ms: 1.12x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.9 ms: 2.45x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| nbody          | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.51 ms: 1.11x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.41 ms: 1.02x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 54.0 ms: 1.01x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.9 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.9 ms: 1.13x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.7 ms: 1.03x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.6 ms: 1.03x slower                                                   |
| tomli_loads          | 957 ms                                                   | 999 ms: 1.04x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.08x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 156 us: 1.12x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.90 ms: 1.15x slower                                                   |
| json_loads           | 10.9 us                                                  | 12.7 us: 1.17x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.55 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.95 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.20x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 24.0 ms: 1.10x slower                                                   |
| mako            | 4.77 ms                                                  | 5.63 ms: 1.18x slower                                                   |
| django_template | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.16x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 784 us: 2.56x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.39x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.27x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 10.0 ms: 2.07x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 88.5 ms: 1.94x faster                                                   |
| mdp                              | 1.09 sec                                                 | 581 ms: 1.88x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 132 ms: 1.69x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 493 us: 1.68x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 238 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                    |
| float                            | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| deepcopy                         | 161 us                                                   | 124 us: 1.30x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.2 us: 1.29x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 829 ns: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                   |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.9 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| k_core                           | 1.12 sec                                                 | 993 ms: 1.13x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.78 us: 1.12x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.1 ms: 1.11x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.51 ms: 1.11x faster                                                   |
| go                               | 70.0 ms                                                  | 63.4 ms: 1.10x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.3 ms: 1.10x faster                                                   |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 202 ms: 1.07x faster                                                    |
| pylint                           | 128 ms                                                   | 120 ms: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 41.6 ms: 1.05x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 52.2 ms: 1.04x faster                                                   |
| pycparser                        | 497 ms                                                   | 480 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.7 ms: 1.03x faster                                                   |
| sphinx                           | 434 ms                                                   | 425 ms: 1.02x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.41 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 54.0 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 98.9 ms: 1.01x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 143 ms: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.10 ms: 1.01x slower                                                   |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.6 ms: 1.02x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.6 ms: 1.03x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 999 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.17 ms: 1.04x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.18 ms: 1.05x slower                                                   |
| thrift                           | 322 us                                                   | 337 us: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                   |
| fannkuch                         | 176 ms                                                   | 184 ms: 1.05x slower                                                    |
| shortest_path                    | 219 ms                                                   | 231 ms: 1.06x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.0 ms: 1.06x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.6 ms: 1.07x slower                                                   |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.07x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 76.3 us: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 230 ms: 1.08x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.08x slower                                                    |
| connected_components             | 201 ms                                                   | 218 ms: 1.09x slower                                                    |
| json                             | 1.93 ms                                                  | 2.10 ms: 1.09x slower                                                   |
| 2to3                             | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 360 ms: 1.10x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 24.0 ms: 1.10x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 733 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.9 ms: 1.10x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.9 ms: 1.11x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 156 us: 1.12x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 50.9 ms: 1.12x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 28.4 ms: 1.12x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.92 us: 1.13x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.3 ms: 1.14x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 26.3 ms: 1.14x slower                                                   |
| logging_format                   | 2.80 us                                                  | 3.21 us: 1.14x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 191 ms: 1.15x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.90 ms: 1.15x slower                                                   |
| json_loads                       | 10.9 us                                                  | 12.7 us: 1.17x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 56.0 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.63 ms: 1.18x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.55 ms: 1.19x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.95 ms: 1.22x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 64.1 ms: 1.25x slower                                                   |
| django_template                  | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.40 ms: 1.30x slower                                                   |
| many_optionals                   | 195 us                                                   | 261 us: 1.34x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 582 us: 1.39x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.7 ms: 1.51x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.9 ms: 2.45x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 217 ns: 4.25x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (2): docutils, async_tree_eager_memoization_tg
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.075x faster

# HPT report

- Reliability score: 86.74% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x