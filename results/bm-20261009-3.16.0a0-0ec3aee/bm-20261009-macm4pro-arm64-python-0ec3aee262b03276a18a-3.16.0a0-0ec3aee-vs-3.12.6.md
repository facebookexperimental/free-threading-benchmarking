# Results vs. 3.12.6

- fork: python
- ref: 0ec3aee262b03276a18a
- machine: darwin-arm64
- commit hash: 0ec3aee
- commit date: 2026-10-09
- overall geometric mean: 1.161x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.04x slower                                                    |
| docutils       | 1.02 sec                                                 | 950 ms: 1.08x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.2 ms: 1.09x faster                                                   |
| sphinx         | 434 ms                                                   | 397 ms: 1.09x faster                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 305 ms: 1.62x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 308 ms: 1.49x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 119 ms: 1.49x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 325 ms: 1.48x faster                                                    |
| async_generators                 | 206 ms                                                   | 144 ms: 1.43x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.68 ms: 1.40x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 124 ms: 1.39x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 330 ms: 1.35x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 172 ms: 1.34x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 280 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 290 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 116 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.9 ms: 1.11x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 261 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 153 ms: 1.36x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 103 ms: 3.20x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.8 ms: 1.36x faster                                                   |
| nbody          | 54.2 ms                                                  | 42.6 ms: 1.27x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.19x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 91.5 ms: 1.09x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.22 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 54.0 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.8 ms: 1.20x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.58 ms: 1.19x faster                                                   |
| tomli_loads          | 957 ms                                                   | 809 ms: 1.18x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 93.7 us: 1.10x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.4 us: 1.05x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 65.3 ms: 1.04x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 137 us: 1.01x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.05 ms: 1.13x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.60 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.45 ms: 1.07x faster                                                   |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.00x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.09 ms: 5.08x faster                                                   |
| pylint                           | 128 ms                                                   | 55.2 ms: 2.32x faster                                                   |
| mdp                              | 1.09 sec                                                 | 502 ms: 2.17x faster                                                    |
| deepcopy                         | 161 us                                                   | 96.8 us: 1.67x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 305 ms: 1.62x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.8 us: 1.56x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.52 us: 1.51x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 308 ms: 1.49x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 119 ms: 1.49x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 325 ms: 1.48x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 48.6 us: 1.46x faster                                                   |
| async_generators                 | 206 ms                                                   | 144 ms: 1.43x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.42x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.68 ms: 1.40x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 124 ms: 1.39x faster                                                    |
| float                            | 37.9 ms                                                  | 27.8 ms: 1.36x faster                                                   |
| async_tree_eager_io_tg           | 446 ms                                                   | 330 ms: 1.35x faster                                                    |
| go                               | 70.0 ms                                                  | 52.0 ms: 1.35x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 172 ms: 1.34x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 41.2 ms: 1.32x faster                                                   |
| generators                       | 21.9 ms                                                  | 16.9 ms: 1.30x faster                                                   |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                    |
| nbody                            | 54.2 ms                                                  | 42.6 ms: 1.27x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.27x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 113 ms: 1.26x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.1 ms: 1.24x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 49.5 ms: 1.23x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.9 ns: 1.21x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.8 ms: 1.20x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.33 us: 1.20x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.14 us: 1.20x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 26.9 ms: 1.20x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.74 ms: 1.20x faster                                                   |
| pyflate                          | 216 ms                                                   | 181 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 280 ms: 1.19x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.58 ms: 1.19x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 809 ms: 1.18x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.18x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 290 ms: 1.17x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.9 ms: 1.16x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.64 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| k_core                           | 1.12 sec                                                 | 972 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 116 ms: 1.14x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                   |
| richards                         | 22.4 ms                                                  | 20.1 ms: 1.12x faster                                                   |
| fannkuch                         | 176 ms                                                   | 157 ms: 1.12x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.9 ms: 1.11x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 22.9 ms: 1.11x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 46.6 ms: 1.10x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 93.7 us: 1.10x faster                                                   |
| sphinx                           | 434 ms                                                   | 397 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.36 ms: 1.09x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 91.5 ms: 1.09x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 21.2 ms: 1.09x faster                                                   |
| docutils                         | 1.02 sec                                                 | 950 ms: 1.08x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.45 ms: 1.07x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                   |
| thrift                           | 322 us                                                   | 303 us: 1.06x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 914 ns: 1.06x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 310 ms: 1.06x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.0 ms: 1.05x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 54.8 ms: 1.05x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.4 us: 1.05x faster                                                   |
| json                             | 1.93 ms                                                  | 1.85 ms: 1.04x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 639 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.22 ms: 1.04x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 65.3 ms: 1.04x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 1.93 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| pycparser                        | 497 ms                                                   | 484 ms: 1.03x faster                                                    |
| bench_thread_pool                | 419 us                                                   | 408 us: 1.03x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 137 us: 1.01x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 54.0 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 833 us: 1.00x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.7 ms: 1.02x slower                                                   |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                    |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                    |
| 2to3                             | 114 ms                                                   | 119 ms: 1.04x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.90 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.8 ms: 1.13x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.05 ms: 1.13x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.60 ms: 1.16x slower                                                   |
| many_optionals                   | 195 us                                                   | 233 us: 1.19x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 261 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 153 ms: 1.36x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 103 ms: 3.20x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                            |
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261009-3.16.0a0-0ec3aee/bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.161x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.18x