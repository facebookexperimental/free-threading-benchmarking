# Results vs. 3.12.6

- fork: python
- ref: 7f371ed84ba471bb1b11
- machine: darwin-arm64
- commit hash: 7f371ed
- commit date: 2025-10-16
- overall geometric mean: 1.120x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                    |
| sphinx         | 434 ms                                                   | 403 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.06x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.94x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 249 ms: 1.85x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 251 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.66x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.92 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.4 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.6 ms: 2.66x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                    |
| nbody          | 54.2 ms                                                  | 47.5 ms: 1.14x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.14x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.1 ms: 1.18x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.7 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.94 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.7 ms: 1.15x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.1 ms: 1.14x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.80 ms: 1.12x faster                                                    |
| tomli_loads          | 957 ms                                                   | 867 ms: 1.10x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 62.0 ms: 1.09x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 98.4 us: 1.05x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 139 us: 1.01x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.88 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.36 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.65 ms: 1.09x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| mako            | 4.77 ms                                                  | 4.69 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.06x faster                                                     |
| mdp                              | 1.09 sec                                                 | 537 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.94x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 249 ms: 1.85x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 251 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.66x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.59x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                     |
| deepcopy                         | 161 us                                                   | 103 us: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.92 ms: 1.37x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.20 us: 1.37x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.09 us: 1.34x faster                                                    |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                    |
| go                               | 70.0 ms                                                  | 53.5 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 39.7 ns: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                     |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.8 ms: 1.24x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.9 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.6 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 46.1 ms: 1.18x faster                                                    |
| pyflate                          | 216 ms                                                   | 184 ms: 1.18x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 37.1 ms: 1.17x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 121 ms: 1.17x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 17.8 ms: 1.17x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.48 ms: 1.16x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.0 ms: 1.16x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.7 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| nbody                            | 54.2 ms                                                  | 47.5 ms: 1.14x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.1 ms: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.4 us: 1.14x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.14x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.27 us: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 985 ms: 1.13x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.83 ms: 1.13x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.47 us: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.4 ms: 1.13x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.6 ms: 1.12x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.80 ms: 1.12x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.71 ms: 1.12x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.0 ms: 1.11x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 867 ms: 1.10x faster                                                     |
| richards                         | 22.4 ms                                                  | 20.4 ms: 1.10x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 62.0 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.33 ms: 1.09x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 47.2 ms: 1.09x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.65 ms: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 403 ms: 1.08x faster                                                     |
| sympy_str                        | 104 ms                                                   | 97.1 ms: 1.07x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 631 ms: 1.05x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 54.7 ms: 1.05x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 312 ms: 1.05x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| thrift                           | 322 us                                                   | 307 us: 1.05x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 98.4 us: 1.05x faster                                                    |
| pycparser                        | 497 ms                                                   | 477 ms: 1.04x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 95.7 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| bench_thread_pool                | 419 us                                                   | 407 us: 1.03x faster                                                     |
| sympy_expand                     | 167 ms                                                   | 164 ms: 1.02x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.69 ms: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 956 ns: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 139 us: 1.01x faster                                                     |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                     |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.0 ms: 1.03x slower                                                    |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.03x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.94 ms: 1.04x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 42.8 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.83 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.88 ms: 1.11x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.36 ms: 1.11x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 928 us: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.2 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 370 us: 1.90x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.6 ms: 2.66x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                             |

Benchmark hidden because not significant (3): 2to3, json, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251016-3.15.0a1+-7f371ed/bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.120x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.18x