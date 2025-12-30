# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: d84384d
- commit date: 2025-12-30
- overall geometric mean: 1.220x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                         |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                       |
| html5lib       | 23.0 ms                                                  | 20.6 ms: 1.11x faster                                                        |
| sphinx         | 434 ms                                                   | 404 ms: 1.07x faster                                                         |
| Geometric mean | (ref)                                                    | 1.04x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 216 ms: 2.30x faster                                                         |
| async_tree_io_tg                 | 480 ms                                                   | 211 ms: 2.27x faster                                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 213 ms: 2.09x faster                                                         |
| async_tree_io                    | 459 ms                                                   | 226 ms: 2.03x faster                                                         |
| async_tree_none                  | 178 ms                                                   | 96.8 ms: 1.84x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 93.7 ms: 1.84x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 131 ms: 1.76x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 134 ms: 1.66x faster                                                         |
| coroutines                       | 13.6 ms                                                  | 9.57 ms: 1.42x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.35x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 250 ms: 1.35x faster                                                         |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                         |
| async_tree_eager                 | 45.6 ms                                                  | 39.0 ms: 1.17x faster                                                        |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                         |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.6 ms: 2.45x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 24.4 ms: 1.55x faster                                                        |
| nbody          | 54.2 ms                                                  | 39.7 ms: 1.36x faster                                                        |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                    | 1.27x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.6 ms: 1.17x faster                                                        |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                        |
| regex_dna      | 99.6 ms                                                  | 96.8 ms: 1.03x faster                                                        |
| regex_v8       | 9.59 ms                                                  | 9.79 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                    | 1.08x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|----------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_pure_python | 103 us                                                   | 72.7 us: 1.42x faster                                                        |
| xml_etree_iterparse  | 51.6 ms                                                  | 37.1 ms: 1.39x faster                                                        |
| pickle_pure_python   | 139 us                                                   | 111 us: 1.25x faster                                                         |
| xml_etree_process    | 26.7 ms                                                  | 22.4 ms: 1.19x faster                                                        |
| tomli_loads          | 957 ms                                                   | 806 ms: 1.19x faster                                                         |
| xml_etree_generate   | 38.9 ms                                                  | 33.3 ms: 1.17x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.69 ms: 1.15x faster                                                        |
| xml_etree_parse      | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                        |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.20x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.06 ms: 1.13x slower                                                        |
| python_startup_no_site | 5.71 ms                                                  | 6.51 ms: 1.14x slower                                                        |
| Geometric mean         | (ref)                                                    | 1.14x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|-----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.16 ms: 1.15x faster                                                        |
| genshi_text     | 10.5 ms                                                  | 9.36 ms: 1.12x faster                                                        |
| django_template | 13.6 ms                                                  | 13.1 ms: 1.04x faster                                                        |
| genshi_xml      | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                        |
| Geometric mean  | (ref)                                                    | 1.07x faster                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.93 ms: 5.28x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 216 ms: 2.30x faster                                                         |
| async_tree_io_tg                 | 480 ms                                                   | 211 ms: 2.27x faster                                                         |
| richards                         | 22.4 ms                                                  | 10.1 ms: 2.22x faster                                                        |
| richards_super                   | 25.4 ms                                                  | 11.9 ms: 2.13x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 213 ms: 2.09x faster                                                         |
| async_tree_io                    | 459 ms                                                   | 226 ms: 2.03x faster                                                         |
| async_tree_none                  | 178 ms                                                   | 96.8 ms: 1.84x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 93.7 ms: 1.84x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 131 ms: 1.76x faster                                                         |
| mdp                              | 1.09 sec                                                 | 642 ms: 1.70x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 134 ms: 1.66x faster                                                         |
| deltablue                        | 1.73 ms                                                  | 1.07 ms: 1.61x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.4 us: 1.61x faster                                                        |
| deepcopy                         | 161 us                                                   | 101 us: 1.60x faster                                                         |
| float                            | 37.9 ms                                                  | 24.4 ms: 1.55x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 40.0 ms: 1.53x faster                                                        |
| logging_silent                   | 50.9 ns                                                  | 34.1 ns: 1.49x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.01 us: 1.44x faster                                                        |
| go                               | 70.0 ms                                                  | 48.9 ms: 1.43x faster                                                        |
| pyflate                          | 216 ms                                                   | 152 ms: 1.42x faster                                                         |
| coroutines                       | 13.6 ms                                                  | 9.57 ms: 1.42x faster                                                        |
| unpickle_pure_python             | 103 us                                                   | 72.7 us: 1.42x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 1.82 us: 1.42x faster                                                        |
| logging_format                   | 2.80 us                                                  | 1.98 us: 1.41x faster                                                        |
| raytrace                         | 145 ms                                                   | 103 ms: 1.40x faster                                                         |
| scimark_lu                       | 51.3 ms                                                  | 36.8 ms: 1.39x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.1 ms: 1.39x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 103 ms: 1.38x faster                                                         |
| nbody                            | 54.2 ms                                                  | 39.7 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.35x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 250 ms: 1.35x faster                                                         |
| scimark_monte_carlo              | 32.2 ms                                                  | 23.8 ms: 1.35x faster                                                        |
| chaos                            | 28.9 ms                                                  | 21.6 ms: 1.34x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 41.2 ms: 1.32x faster                                                        |
| k_core                           | 1.12 sec                                                 | 869 ms: 1.29x faster                                                         |
| comprehensions                   | 9.84 us                                                  | 7.72 us: 1.27x faster                                                        |
| pickle_pure_python               | 139 us                                                   | 111 us: 1.25x faster                                                         |
| crypto_pyaes                     | 38.8 ms                                                  | 31.3 ms: 1.24x faster                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 265 ms: 1.24x faster                                                         |
| pprint_pformat                   | 665 ms                                                   | 543 ms: 1.22x faster                                                         |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                         |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.87 sec: 1.19x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 22.4 ms: 1.19x faster                                                        |
| tomli_loads                      | 957 ms                                                   | 806 ms: 1.19x faster                                                         |
| regex_compile                    | 54.6 ms                                                  | 46.6 ms: 1.17x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 39.0 ms: 1.17x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 33.3 ms: 1.17x faster                                                        |
| json_dumps                       | 4.26 ms                                                  | 3.69 ms: 1.15x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                        |
| mako                             | 4.77 ms                                                  | 4.16 ms: 1.15x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 62.0 us: 1.14x faster                                                        |
| fannkuch                         | 176 ms                                                   | 154 ms: 1.14x faster                                                         |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                        |
| genshi_text                      | 10.5 ms                                                  | 9.36 ms: 1.12x faster                                                        |
| thrift                           | 322 us                                                   | 287 us: 1.12x faster                                                         |
| html5lib                         | 23.0 ms                                                  | 20.6 ms: 1.11x faster                                                        |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                         |
| generators                       | 21.9 ms                                                  | 19.9 ms: 1.10x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 39.6 ms: 1.10x faster                                                        |
| sphinx                           | 434 ms                                                   | 404 ms: 1.07x faster                                                         |
| xml_etree_parse                  | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                        |
| pycparser                        | 497 ms                                                   | 470 ms: 1.06x faster                                                         |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.97 ms: 1.05x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                         |
| django_template                  | 13.6 ms                                                  | 13.1 ms: 1.04x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 96.8 ms: 1.03x faster                                                        |
| meteor_contest                   | 47.7 ms                                                  | 46.5 ms: 1.03x faster                                                        |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                        |
| telco                            | 2.61 ms                                                  | 2.57 ms: 1.01x faster                                                        |
| connected_components             | 201 ms                                                   | 198 ms: 1.01x faster                                                         |
| hexiom                           | 3.04 ms                                                  | 3.01 ms: 1.01x faster                                                        |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                        |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                         |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                         |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                         |
| sqlite_synth                     | 967 ns                                                   | 974 ns: 1.01x slower                                                         |
| regex_v8                         | 9.59 ms                                                  | 9.79 ms: 1.02x slower                                                        |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                       |
| genshi_xml                       | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                        |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                         |
| bench_thread_pool                | 419 us                                                   | 434 us: 1.04x slower                                                         |
| gc_traversal                     | 2.01 ms                                                  | 2.10 ms: 1.04x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                         |
| sympy_integrate                  | 8.02 ms                                                  | 8.58 ms: 1.07x slower                                                        |
| pylint                           | 128 ms                                                   | 140 ms: 1.09x slower                                                         |
| sympy_expand                     | 167 ms                                                   | 184 ms: 1.10x slower                                                         |
| python_startup                   | 8.01 ms                                                  | 9.06 ms: 1.13x slower                                                        |
| create_gc_cycles                 | 830 us                                                   | 942 us: 1.13x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                         |
| sympy_sum                        | 57.6 ms                                                  | 65.6 ms: 1.14x slower                                                        |
| python_startup_no_site           | 5.71 ms                                                  | 6.51 ms: 1.14x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 45.5 ms: 1.15x slower                                                        |
| sympy_str                        | 104 ms                                                   | 122 ms: 1.17x slower                                                         |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                        |
| many_optionals                   | 195 us                                                   | 258 us: 1.32x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.6 ms: 2.45x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                                 |
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251230-3.15.0a3+-d84384d-JIT/bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.220x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.12x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.25x