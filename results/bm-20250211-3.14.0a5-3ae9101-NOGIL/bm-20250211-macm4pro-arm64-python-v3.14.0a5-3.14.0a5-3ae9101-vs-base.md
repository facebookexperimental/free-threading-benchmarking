# Results vs. base

- fork: python
- ref: v3.14.0a5
- machine: darwin-arm64
- commit hash: 3ae9101
- commit date: 2025-02-11
- overall geometric mean: 1.094x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250211-3.14.0a5-3ae9101/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json | results/bm-20250211-3.14.0a5-3ae9101-NOGIL/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json |
|----------------|:------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| 2to3           | 110 ms                                                                                                 | 128 ms: 1.16x slower                                                                                         |
| docutils       | 1.04 sec                                                                                               | 1.03 sec: 1.01x faster                                                                                       |
| html5lib       | 22.1 ms                                                                                                | 23.9 ms: 1.08x slower                                                                                        |
| sphinx         | 409 ms                                                                                                 | 437 ms: 1.07x slower                                                                                         |
| Geometric mean | (ref)                                                                                                  | 1.07x slower                                                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20250211-3.14.0a5-3ae9101/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json | results/bm-20250211-3.14.0a5-3ae9101-NOGIL/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json |
|----------------------------------|:------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 267 ms                                                                                                 | 219 ms: 1.22x faster                                                                                         |
| async_tree_io_tg                 | 262 ms                                                                                                 | 222 ms: 1.18x faster                                                                                         |
| async_tree_eager_io              | 255 ms                                                                                                 | 230 ms: 1.11x faster                                                                                         |
| async_tree_none_tg               | 111 ms                                                                                                 | 99.9 ms: 1.11x faster                                                                                        |
| async_tree_io                    | 262 ms                                                                                                 | 238 ms: 1.10x faster                                                                                         |
| async_tree_cpu_io_mixed_tg       | 266 ms                                                                                                 | 242 ms: 1.10x faster                                                                                         |
| async_tree_memoization_tg        | 153 ms                                                                                                 | 140 ms: 1.09x faster                                                                                         |
| async_tree_eager_memoization_tg  | 139 ms                                                                                                 | 127 ms: 1.09x faster                                                                                         |
| async_tree_eager_cpu_io_mixed_tg | 247 ms                                                                                                 | 232 ms: 1.07x faster                                                                                         |
| async_tree_cpu_io_mixed          | 266 ms                                                                                                 | 252 ms: 1.05x faster                                                                                         |
| async_tree_eager_tg              | 92.7 ms                                                                                                | 89.6 ms: 1.03x faster                                                                                        |
| asyncio_websockets               | 193 ms                                                                                                 | 186 ms: 1.03x faster                                                                                         |
| async_tree_memoization           | 153 ms                                                                                                 | 149 ms: 1.03x faster                                                                                         |
| async_tree_none                  | 118 ms                                                                                                 | 115 ms: 1.02x faster                                                                                         |
| async_tree_eager_cpu_io_mixed    | 221 ms                                                                                                 | 229 ms: 1.04x slower                                                                                         |
| async_generators                 | 175 ms                                                                                                 | 186 ms: 1.07x slower                                                                                         |
| async_tree_eager_memoization     | 115 ms                                                                                                 | 124 ms: 1.08x slower                                                                                         |
| coroutines                       | 10.2 ms                                                                                                | 11.3 ms: 1.11x slower                                                                                        |
| async_tree_eager                 | 44.0 ms                                                                                                | 57.7 ms: 1.31x slower                                                                                        |
| Geometric mean                   | (ref)                                                                                                  | 1.03x faster                                                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250211-3.14.0a5-3ae9101/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json | results/bm-20250211-3.14.0a5-3ae9101-NOGIL/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json |
|----------------|:------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| pidigits       | 164 ms                                                                                                 | 159 ms: 1.03x faster                                                                                         |
| float          | 31.5 ms                                                                                                | 34.2 ms: 1.09x slower                                                                                        |
| nbody          | 50.0 ms                                                                                                | 72.6 ms: 1.45x slower                                                                                        |
| Geometric mean | (ref)                                                                                                  | 1.15x slower                                                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250211-3.14.0a5-3ae9101/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json | results/bm-20250211-3.14.0a5-3ae9101-NOGIL/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json |
|----------------|:------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 10.8 ms                                                                                                | 10.3 ms: 1.05x faster                                                                                        |
| regex_effbot   | 1.45 ms                                                                                                | 1.42 ms: 1.02x faster                                                                                        |
| regex_dna      | 93.6 ms                                                                                                | 91.7 ms: 1.02x faster                                                                                        |
| regex_compile  | 47.4 ms                                                                                                | 57.3 ms: 1.21x slower                                                                                        |
| Geometric mean | (ref)                                                                                                  | 1.03x slower                                                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250211-3.14.0a5-3ae9101/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json | results/bm-20250211-3.14.0a5-3ae9101-NOGIL/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json |
|----------------------|:------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                                                                | 41.2 ms: 1.12x faster                                                                                        |
| xml_etree_parse      | 62.1 ms                                                                                                | 57.6 ms: 1.08x faster                                                                                        |
| json_dumps           | 5.02 ms                                                                                                | 5.13 ms: 1.02x slower                                                                                        |
| json_loads           | 11.4 us                                                                                                | 11.8 us: 1.03x slower                                                                                        |
| xml_etree_generate   | 36.5 ms                                                                                                | 40.5 ms: 1.11x slower                                                                                        |
| xml_etree_process    | 26.4 ms                                                                                                | 29.7 ms: 1.13x slower                                                                                        |
| pickle_pure_python   | 139 us                                                                                                 | 173 us: 1.24x slower                                                                                         |
| unpickle_pure_python | 99.7 us                                                                                                | 127 us: 1.27x slower                                                                                         |
| tomli_loads          | 826 ms                                                                                                 | 1.07 sec: 1.29x slower                                                                                       |
| Geometric mean       | (ref)                                                                                                  | 1.09x slower                                                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250211-3.14.0a5-3ae9101/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json | results/bm-20250211-3.14.0a5-3ae9101-NOGIL/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json |
|------------------------|:------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| python_startup         | 8.60 ms                                                                                                | 9.26 ms: 1.08x slower                                                                                        |
| python_startup_no_site | 5.98 ms                                                                                                | 6.68 ms: 1.12x slower                                                                                        |
| Geometric mean         | (ref)                                                                                                  | 1.10x slower                                                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250211-3.14.0a5-3ae9101/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json | results/bm-20250211-3.14.0a5-3ae9101-NOGIL/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json |
|-----------------|:------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| django_template | 15.2 ms                                                                                                | 17.9 ms: 1.18x slower                                                                                        |
| genshi_xml      | 20.7 ms                                                                                                | 25.9 ms: 1.25x slower                                                                                        |
| genshi_text     | 10.1 ms                                                                                                | 12.7 ms: 1.26x slower                                                                                        |
| mako            | 4.73 ms                                                                                                | 6.22 ms: 1.31x slower                                                                                        |
| Geometric mean  | (ref)                                                                                                  | 1.25x slower                                                                                                 |

All benchmarks:
===============

| Benchmark                        | results/bm-20250211-3.14.0a5-3ae9101/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json | results/bm-20250211-3.14.0a5-3ae9101-NOGIL/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json |
|----------------------------------|:------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| gc_traversal                     | 2.10 ms                                                                                                | 906 us: 2.32x faster                                                                                         |
| create_gc_cycles                 | 903 us                                                                                                 | 494 us: 1.83x faster                                                                                         |
| async_tree_eager_io_tg           | 267 ms                                                                                                 | 219 ms: 1.22x faster                                                                                         |
| async_tree_io_tg                 | 262 ms                                                                                                 | 222 ms: 1.18x faster                                                                                         |
| sqlite_synth                     | 954 ns                                                                                                 | 848 ns: 1.12x faster                                                                                         |
| xml_etree_iterparse              | 46.1 ms                                                                                                | 41.2 ms: 1.12x faster                                                                                        |
| async_tree_eager_io              | 255 ms                                                                                                 | 230 ms: 1.11x faster                                                                                         |
| async_tree_none_tg               | 111 ms                                                                                                 | 99.9 ms: 1.11x faster                                                                                        |
| async_tree_io                    | 262 ms                                                                                                 | 238 ms: 1.10x faster                                                                                         |
| async_tree_cpu_io_mixed_tg       | 266 ms                                                                                                 | 242 ms: 1.10x faster                                                                                         |
| async_tree_memoization_tg        | 153 ms                                                                                                 | 140 ms: 1.09x faster                                                                                         |
| async_tree_eager_memoization_tg  | 139 ms                                                                                                 | 127 ms: 1.09x faster                                                                                         |
| xml_etree_parse                  | 62.1 ms                                                                                                | 57.6 ms: 1.08x faster                                                                                        |
| async_tree_eager_cpu_io_mixed_tg | 247 ms                                                                                                 | 232 ms: 1.07x faster                                                                                         |
| async_tree_cpu_io_mixed          | 266 ms                                                                                                 | 252 ms: 1.05x faster                                                                                         |
| regex_v8                         | 10.8 ms                                                                                                | 10.3 ms: 1.05x faster                                                                                        |
| async_tree_eager_tg              | 92.7 ms                                                                                                | 89.6 ms: 1.03x faster                                                                                        |
| asyncio_websockets               | 193 ms                                                                                                 | 186 ms: 1.03x faster                                                                                         |
| async_tree_memoization           | 153 ms                                                                                                 | 149 ms: 1.03x faster                                                                                         |
| pidigits                         | 164 ms                                                                                                 | 159 ms: 1.03x faster                                                                                         |
| regex_effbot                     | 1.45 ms                                                                                                | 1.42 ms: 1.02x faster                                                                                        |
| regex_dna                        | 93.6 ms                                                                                                | 91.7 ms: 1.02x faster                                                                                        |
| async_tree_none                  | 118 ms                                                                                                 | 115 ms: 1.02x faster                                                                                         |
| docutils                         | 1.04 sec                                                                                               | 1.03 sec: 1.01x faster                                                                                       |
| json                             | 1.95 ms                                                                                                | 1.98 ms: 1.01x slower                                                                                        |
| pathlib                          | 11.2 ms                                                                                                | 11.4 ms: 1.02x slower                                                                                        |
| json_dumps                       | 5.02 ms                                                                                                | 5.13 ms: 1.02x slower                                                                                        |
| json_loads                       | 11.4 us                                                                                                | 11.8 us: 1.03x slower                                                                                        |
| async_tree_eager_cpu_io_mixed    | 221 ms                                                                                                 | 229 ms: 1.04x slower                                                                                         |
| bench_mp_pool                    | 36.6 ms                                                                                                | 38.0 ms: 1.04x slower                                                                                        |
| pycparser                        | 481 ms                                                                                                 | 502 ms: 1.04x slower                                                                                         |
| async_generators                 | 175 ms                                                                                                 | 186 ms: 1.07x slower                                                                                         |
| sphinx                           | 409 ms                                                                                                 | 437 ms: 1.07x slower                                                                                         |
| many_optionals                   | 229 us                                                                                                 | 246 us: 1.07x slower                                                                                         |
| pylint                           | 115 ms                                                                                                 | 123 ms: 1.08x slower                                                                                         |
| subparsers                       | 8.42 ms                                                                                                | 9.05 ms: 1.08x slower                                                                                        |
| python_startup                   | 8.60 ms                                                                                                | 9.26 ms: 1.08x slower                                                                                        |
| html5lib                         | 22.1 ms                                                                                                | 23.9 ms: 1.08x slower                                                                                        |
| async_tree_eager_memoization     | 115 ms                                                                                                 | 124 ms: 1.08x slower                                                                                         |
| bpe_tokeniser                    | 1.99 sec                                                                                               | 2.16 sec: 1.08x slower                                                                                       |
| float                            | 31.5 ms                                                                                                | 34.2 ms: 1.09x slower                                                                                        |
| mdp                              | 1.08 sec                                                                                               | 1.17 sec: 1.09x slower                                                                                       |
| k_core                           | 943 ms                                                                                                 | 1.03 sec: 1.09x slower                                                                                       |
| dulwich_log                      | 19.9 ms                                                                                                | 21.9 ms: 1.10x slower                                                                                        |
| xml_etree_generate               | 36.5 ms                                                                                                | 40.5 ms: 1.11x slower                                                                                        |
| coroutines                       | 10.2 ms                                                                                                | 11.3 ms: 1.11x slower                                                                                        |
| sqlglot_optimize                 | 23.1 ms                                                                                                | 25.8 ms: 1.12x slower                                                                                        |
| python_startup_no_site           | 5.98 ms                                                                                                | 6.68 ms: 1.12x slower                                                                                        |
| sqlglot_normalize                | 124 ms                                                                                                 | 140 ms: 1.12x slower                                                                                         |
| telco                            | 3.17 ms                                                                                                | 3.56 ms: 1.13x slower                                                                                        |
| xml_etree_process                | 26.4 ms                                                                                                | 29.7 ms: 1.13x slower                                                                                        |
| thrift                           | 312 us                                                                                                 | 352 us: 1.13x slower                                                                                         |
| shortest_path                    | 216 ms                                                                                                 | 247 ms: 1.14x slower                                                                                         |
| sqlalchemy_imperative            | 5.11 ms                                                                                                | 5.85 ms: 1.14x slower                                                                                        |
| sympy_sum                        | 54.6 ms                                                                                                | 63.1 ms: 1.15x slower                                                                                        |
| pyflate                          | 199 ms                                                                                                 | 230 ms: 1.15x slower                                                                                         |
| sqlalchemy_declarative           | 44.3 ms                                                                                                | 51.1 ms: 1.16x slower                                                                                        |
| coverage                         | 32.8 ms                                                                                                | 38.0 ms: 1.16x slower                                                                                        |
| 2to3                             | 110 ms                                                                                                 | 128 ms: 1.16x slower                                                                                         |
| meteor_contest                   | 48.0 ms                                                                                                | 56.0 ms: 1.17x slower                                                                                        |
| sympy_integrate                  | 7.96 ms                                                                                                | 9.29 ms: 1.17x slower                                                                                        |
| connected_components             | 199 ms                                                                                                 | 233 ms: 1.17x slower                                                                                         |
| sympy_expand                     | 168 ms                                                                                                 | 197 ms: 1.17x slower                                                                                         |
| nqueens                          | 40.6 ms                                                                                                | 47.8 ms: 1.18x slower                                                                                        |
| django_template                  | 15.2 ms                                                                                                | 17.9 ms: 1.18x slower                                                                                        |
| sympy_str                        | 99.8 ms                                                                                                | 119 ms: 1.19x slower                                                                                         |
| chaos                            | 27.3 ms                                                                                                | 32.7 ms: 1.20x slower                                                                                        |
| deepcopy                         | 104 us                                                                                                 | 125 us: 1.20x slower                                                                                         |
| crypto_pyaes                     | 36.6 ms                                                                                                | 44.2 ms: 1.21x slower                                                                                        |
| regex_compile                    | 47.4 ms                                                                                                | 57.3 ms: 1.21x slower                                                                                        |
| logging_format                   | 2.59 us                                                                                                | 3.14 us: 1.21x slower                                                                                        |
| logging_simple                   | 2.33 us                                                                                                | 2.87 us: 1.23x slower                                                                                        |
| deepcopy_reduce                  | 1.11 us                                                                                                | 1.36 us: 1.23x slower                                                                                        |
| pickle_pure_python               | 139 us                                                                                                 | 173 us: 1.24x slower                                                                                         |
| fannkuch                         | 172 ms                                                                                                 | 213 ms: 1.24x slower                                                                                         |
| sqlglot_transpile                | 653 us                                                                                                 | 812 us: 1.24x slower                                                                                         |
| genshi_xml                       | 20.7 ms                                                                                                | 25.9 ms: 1.25x slower                                                                                        |
| richards                         | 21.7 ms                                                                                                | 27.1 ms: 1.25x slower                                                                                        |
| genshi_text                      | 10.1 ms                                                                                                | 12.7 ms: 1.26x slower                                                                                        |
| sqlglot_parse                    | 533 us                                                                                                 | 675 us: 1.27x slower                                                                                         |
| logging_silent                   | 43.4 ns                                                                                                | 55.0 ns: 1.27x slower                                                                                        |
| spectral_norm                    | 44.8 ms                                                                                                | 56.7 ms: 1.27x slower                                                                                        |
| richards_super                   | 24.4 ms                                                                                                | 31.0 ms: 1.27x slower                                                                                        |
| go                               | 56.9 ms                                                                                                | 72.2 ms: 1.27x slower                                                                                        |
| unpickle_pure_python             | 99.7 us                                                                                                | 127 us: 1.27x slower                                                                                         |
| typing_runtime_protocols         | 64.9 us                                                                                                | 82.6 us: 1.27x slower                                                                                        |
| raytrace                         | 124 ms                                                                                                 | 158 ms: 1.28x slower                                                                                         |
| pprint_safe_repr                 | 320 ms                                                                                                 | 409 ms: 1.28x slower                                                                                         |
| comprehensions                   | 7.44 us                                                                                                | 9.58 us: 1.29x slower                                                                                        |
| tomli_loads                      | 826 ms                                                                                                 | 1.07 sec: 1.29x slower                                                                                       |
| generators                       | 17.5 ms                                                                                                | 22.6 ms: 1.29x slower                                                                                        |
| scimark_fft                      | 124 ms                                                                                                 | 161 ms: 1.30x slower                                                                                         |
| pprint_pformat                   | 644 ms                                                                                                 | 836 ms: 1.30x slower                                                                                         |
| scimark_sor                      | 53.4 ms                                                                                                | 69.7 ms: 1.31x slower                                                                                        |
| deepcopy_memo                    | 12.5 us                                                                                                | 16.3 us: 1.31x slower                                                                                        |
| async_tree_eager                 | 44.0 ms                                                                                                | 57.7 ms: 1.31x slower                                                                                        |
| mako                             | 4.73 ms                                                                                                | 6.22 ms: 1.31x slower                                                                                        |
| scimark_monte_carlo              | 30.6 ms                                                                                                | 40.6 ms: 1.33x slower                                                                                        |
| deltablue                        | 1.55 ms                                                                                                | 2.08 ms: 1.34x slower                                                                                        |
| hexiom                           | 2.91 ms                                                                                                | 3.92 ms: 1.35x slower                                                                                        |
| scimark_lu                       | 48.3 ms                                                                                                | 65.4 ms: 1.35x slower                                                                                        |
| scimark_sparse_mat_mult          | 1.74 ms                                                                                                | 2.53 ms: 1.45x slower                                                                                        |
| nbody                            | 50.0 ms                                                                                                | 72.6 ms: 1.45x slower                                                                                        |
| bench_thread_pool                | 429 us                                                                                                 | 626 us: 1.46x slower                                                                                         |
| Geometric mean                   | (ref)                                                                                                  | 1.11x slower                                                                                                 |
Ignored benchmarks (1) of results/bm-20250211-3.14.0a5-3ae9101/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101.json: dask

- Geometric mean (including insignificant results): 1.094x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.10x