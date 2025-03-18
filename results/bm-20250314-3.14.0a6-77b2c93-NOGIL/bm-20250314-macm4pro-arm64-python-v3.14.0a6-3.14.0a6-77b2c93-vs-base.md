# Results vs. base

- fork: python
- ref: v3.14.0a6
- machine: darwin-arm64
- commit hash: 77b2c93
- commit date: 2025-03-14
- overall geometric mean: 1.082x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250314-3.14.0a6-77b2c93/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json | results/bm-20250314-3.14.0a6-77b2c93-NOGIL/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json |
|----------------|:------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                                                                 | 132 ms: 1.15x slower                                                                                         |
| docutils       | 1.07 sec                                                                                               | 1.06 sec: 1.01x faster                                                                                       |
| html5lib       | 22.9 ms                                                                                                | 24.3 ms: 1.06x slower                                                                                        |
| sphinx         | 421 ms                                                                                                 | 440 ms: 1.04x slower                                                                                         |
| Geometric mean | (ref)                                                                                                  | 1.06x slower                                                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20250314-3.14.0a6-77b2c93/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json | results/bm-20250314-3.14.0a6-77b2c93-NOGIL/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json |
|----------------------------------|:------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 268 ms                                                                                                 | 224 ms: 1.20x faster                                                                                         |
| async_tree_io_tg                 | 266 ms                                                                                                 | 225 ms: 1.18x faster                                                                                         |
| async_tree_none_tg               | 112 ms                                                                                                 | 100 ms: 1.12x faster                                                                                         |
| async_tree_eager_io              | 260 ms                                                                                                 | 234 ms: 1.12x faster                                                                                         |
| async_tree_io                    | 266 ms                                                                                                 | 240 ms: 1.11x faster                                                                                         |
| async_tree_memoization_tg        | 155 ms                                                                                                 | 140 ms: 1.11x faster                                                                                         |
| async_tree_cpu_io_mixed_tg       | 270 ms                                                                                                 | 247 ms: 1.10x faster                                                                                         |
| async_tree_eager_memoization_tg  | 139 ms                                                                                                 | 127 ms: 1.09x faster                                                                                         |
| async_tree_eager_cpu_io_mixed_tg | 252 ms                                                                                                 | 235 ms: 1.07x faster                                                                                         |
| async_tree_cpu_io_mixed          | 270 ms                                                                                                 | 256 ms: 1.06x faster                                                                                         |
| async_tree_memoization           | 155 ms                                                                                                 | 149 ms: 1.04x faster                                                                                         |
| async_tree_eager_tg              | 91.8 ms                                                                                                | 88.6 ms: 1.04x faster                                                                                        |
| asyncio_websockets               | 194 ms                                                                                                 | 190 ms: 1.02x faster                                                                                         |
| async_tree_none                  | 117 ms                                                                                                 | 116 ms: 1.01x faster                                                                                         |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                                                                 | 231 ms: 1.03x slower                                                                                         |
| async_tree_eager_memoization     | 117 ms                                                                                                 | 123 ms: 1.06x slower                                                                                         |
| async_generators                 | 179 ms                                                                                                 | 194 ms: 1.08x slower                                                                                         |
| coroutines                       | 10.9 ms                                                                                                | 12.2 ms: 1.13x slower                                                                                        |
| async_tree_eager                 | 43.8 ms                                                                                                | 56.9 ms: 1.30x slower                                                                                        |
| Geometric mean                   | (ref)                                                                                                  | 1.03x faster                                                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250314-3.14.0a6-77b2c93/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json | results/bm-20250314-3.14.0a6-77b2c93-NOGIL/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json |
|----------------|:------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| pidigits       | 163 ms                                                                                                 | 161 ms: 1.02x faster                                                                                         |
| float          | 33.0 ms                                                                                                | 35.9 ms: 1.09x slower                                                                                        |
| nbody          | 51.0 ms                                                                                                | 77.9 ms: 1.53x slower                                                                                        |
| Geometric mean | (ref)                                                                                                  | 1.18x slower                                                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250314-3.14.0a6-77b2c93/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json | results/bm-20250314-3.14.0a6-77b2c93-NOGIL/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json |
|----------------|:------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 10.9 ms                                                                                                | 10.4 ms: 1.05x faster                                                                                        |
| regex_dna      | 92.8 ms                                                                                                | 91.8 ms: 1.01x faster                                                                                        |
| regex_effbot   | 1.45 ms                                                                                                | 1.44 ms: 1.01x faster                                                                                        |
| regex_compile  | 49.0 ms                                                                                                | 59.5 ms: 1.21x slower                                                                                        |
| Geometric mean | (ref)                                                                                                  | 1.03x slower                                                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250314-3.14.0a6-77b2c93/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json | results/bm-20250314-3.14.0a6-77b2c93-NOGIL/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json |
|----------------------|:------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.6 ms                                                                                                | 41.0 ms: 1.14x faster                                                                                        |
| xml_etree_parse      | 62.2 ms                                                                                                | 59.7 ms: 1.04x faster                                                                                        |
| json_dumps           | 5.06 ms                                                                                                | 5.30 ms: 1.05x slower                                                                                        |
| json_loads           | 11.5 us                                                                                                | 12.0 us: 1.05x slower                                                                                        |
| xml_etree_generate   | 37.3 ms                                                                                                | 41.2 ms: 1.10x slower                                                                                        |
| xml_etree_process    | 27.1 ms                                                                                                | 30.5 ms: 1.13x slower                                                                                        |
| pickle_pure_python   | 148 us                                                                                                 | 171 us: 1.16x slower                                                                                         |
| unpickle_pure_python | 105 us                                                                                                 | 128 us: 1.22x slower                                                                                         |
| tomli_loads          | 862 ms                                                                                                 | 1.07 sec: 1.25x slower                                                                                       |
| Geometric mean       | (ref)                                                                                                  | 1.08x slower                                                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250314-3.14.0a6-77b2c93/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json | results/bm-20250314-3.14.0a6-77b2c93-NOGIL/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json |
|------------------------|:------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| python_startup         | 8.66 ms                                                                                                | 9.20 ms: 1.06x slower                                                                                        |
| python_startup_no_site | 6.42 ms                                                                                                | 7.24 ms: 1.13x slower                                                                                        |
| Geometric mean         | (ref)                                                                                                  | 1.09x slower                                                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250314-3.14.0a6-77b2c93/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json | results/bm-20250314-3.14.0a6-77b2c93-NOGIL/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json |
|-----------------|:------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| django_template | 15.7 ms                                                                                                | 18.4 ms: 1.17x slower                                                                                        |
| genshi_xml      | 21.8 ms                                                                                                | 26.1 ms: 1.20x slower                                                                                        |
| genshi_text     | 10.6 ms                                                                                                | 13.0 ms: 1.23x slower                                                                                        |
| mako            | 4.82 ms                                                                                                | 6.19 ms: 1.29x slower                                                                                        |
| Geometric mean  | (ref)                                                                                                  | 1.22x slower                                                                                                 |

All benchmarks:
===============

| Benchmark                        | results/bm-20250314-3.14.0a6-77b2c93/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json | results/bm-20250314-3.14.0a6-77b2c93-NOGIL/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json |
|----------------------------------|:------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| gc_traversal                     | 2.13 ms                                                                                                | 908 us: 2.35x faster                                                                                         |
| create_gc_cycles                 | 900 us                                                                                                 | 480 us: 1.87x faster                                                                                         |
| async_tree_eager_io_tg           | 268 ms                                                                                                 | 224 ms: 1.20x faster                                                                                         |
| async_tree_io_tg                 | 266 ms                                                                                                 | 225 ms: 1.18x faster                                                                                         |
| xml_etree_iterparse              | 46.6 ms                                                                                                | 41.0 ms: 1.14x faster                                                                                        |
| sqlite_synth                     | 950 ns                                                                                                 | 841 ns: 1.13x faster                                                                                         |
| async_tree_none_tg               | 112 ms                                                                                                 | 100 ms: 1.12x faster                                                                                         |
| async_tree_eager_io              | 260 ms                                                                                                 | 234 ms: 1.12x faster                                                                                         |
| async_tree_io                    | 266 ms                                                                                                 | 240 ms: 1.11x faster                                                                                         |
| async_tree_memoization_tg        | 155 ms                                                                                                 | 140 ms: 1.11x faster                                                                                         |
| async_tree_cpu_io_mixed_tg       | 270 ms                                                                                                 | 247 ms: 1.10x faster                                                                                         |
| async_tree_eager_memoization_tg  | 139 ms                                                                                                 | 127 ms: 1.09x faster                                                                                         |
| async_tree_eager_cpu_io_mixed_tg | 252 ms                                                                                                 | 235 ms: 1.07x faster                                                                                         |
| async_tree_cpu_io_mixed          | 270 ms                                                                                                 | 256 ms: 1.06x faster                                                                                         |
| regex_v8                         | 10.9 ms                                                                                                | 10.4 ms: 1.05x faster                                                                                        |
| async_tree_memoization           | 155 ms                                                                                                 | 149 ms: 1.04x faster                                                                                         |
| xml_etree_parse                  | 62.2 ms                                                                                                | 59.7 ms: 1.04x faster                                                                                        |
| async_tree_eager_tg              | 91.8 ms                                                                                                | 88.6 ms: 1.04x faster                                                                                        |
| asyncio_websockets               | 194 ms                                                                                                 | 190 ms: 1.02x faster                                                                                         |
| pidigits                         | 163 ms                                                                                                 | 161 ms: 1.02x faster                                                                                         |
| regex_dna                        | 92.8 ms                                                                                                | 91.8 ms: 1.01x faster                                                                                        |
| regex_effbot                     | 1.45 ms                                                                                                | 1.44 ms: 1.01x faster                                                                                        |
| docutils                         | 1.07 sec                                                                                               | 1.06 sec: 1.01x faster                                                                                       |
| async_tree_none                  | 117 ms                                                                                                 | 116 ms: 1.01x faster                                                                                         |
| pathlib                          | 11.4 ms                                                                                                | 11.6 ms: 1.02x slower                                                                                        |
| pycparser                        | 498 ms                                                                                                 | 510 ms: 1.03x slower                                                                                         |
| bench_mp_pool                    | 37.7 ms                                                                                                | 38.7 ms: 1.03x slower                                                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                                                                 | 231 ms: 1.03x slower                                                                                         |
| json                             | 1.96 ms                                                                                                | 2.02 ms: 1.03x slower                                                                                        |
| sphinx                           | 421 ms                                                                                                 | 440 ms: 1.04x slower                                                                                         |
| json_dumps                       | 5.06 ms                                                                                                | 5.30 ms: 1.05x slower                                                                                        |
| json_loads                       | 11.5 us                                                                                                | 12.0 us: 1.05x slower                                                                                        |
| async_tree_eager_memoization     | 117 ms                                                                                                 | 123 ms: 1.06x slower                                                                                         |
| python_startup                   | 8.66 ms                                                                                                | 9.20 ms: 1.06x slower                                                                                        |
| many_optionals                   | 238 us                                                                                                 | 253 us: 1.06x slower                                                                                         |
| html5lib                         | 22.9 ms                                                                                                | 24.3 ms: 1.06x slower                                                                                        |
| pylint                           | 117 ms                                                                                                 | 125 ms: 1.07x slower                                                                                         |
| subparsers                       | 8.80 ms                                                                                                | 9.41 ms: 1.07x slower                                                                                        |
| bpe_tokeniser                    | 2.09 sec                                                                                               | 2.26 sec: 1.08x slower                                                                                       |
| mdp                              | 1.11 sec                                                                                               | 1.20 sec: 1.08x slower                                                                                       |
| async_generators                 | 179 ms                                                                                                 | 194 ms: 1.08x slower                                                                                         |
| float                            | 33.0 ms                                                                                                | 35.9 ms: 1.09x slower                                                                                        |
| sqlalchemy_imperative            | 5.33 ms                                                                                                | 5.85 ms: 1.10x slower                                                                                        |
| sqlglot_optimize                 | 23.9 ms                                                                                                | 26.2 ms: 1.10x slower                                                                                        |
| xml_etree_generate               | 37.3 ms                                                                                                | 41.2 ms: 1.10x slower                                                                                        |
| k_core                           | 964 ms                                                                                                 | 1.06 sec: 1.10x slower                                                                                       |
| thrift                           | 320 us                                                                                                 | 353 us: 1.10x slower                                                                                         |
| dulwich_log                      | 17.8 ms                                                                                                | 19.6 ms: 1.11x slower                                                                                        |
| sqlglot_normalize                | 128 ms                                                                                                 | 142 ms: 1.11x slower                                                                                         |
| shortest_path                    | 223 ms                                                                                                 | 247 ms: 1.11x slower                                                                                         |
| sympy_sum                        | 56.7 ms                                                                                                | 63.7 ms: 1.12x slower                                                                                        |
| crypto_pyaes                     | 40.4 ms                                                                                                | 45.4 ms: 1.12x slower                                                                                        |
| xml_etree_process                | 27.1 ms                                                                                                | 30.5 ms: 1.13x slower                                                                                        |
| coroutines                       | 10.9 ms                                                                                                | 12.2 ms: 1.13x slower                                                                                        |
| python_startup_no_site           | 6.42 ms                                                                                                | 7.24 ms: 1.13x slower                                                                                        |
| nqueens                          | 44.3 ms                                                                                                | 50.1 ms: 1.13x slower                                                                                        |
| telco                            | 3.16 ms                                                                                                | 3.57 ms: 1.13x slower                                                                                        |
| sqlalchemy_declarative           | 45.3 ms                                                                                                | 51.4 ms: 1.13x slower                                                                                        |
| sympy_integrate                  | 8.23 ms                                                                                                | 9.33 ms: 1.13x slower                                                                                        |
| pyflate                          | 207 ms                                                                                                 | 236 ms: 1.14x slower                                                                                         |
| connected_components             | 206 ms                                                                                                 | 235 ms: 1.15x slower                                                                                         |
| 2to3                             | 114 ms                                                                                                 | 132 ms: 1.15x slower                                                                                         |
| pickle_pure_python               | 148 us                                                                                                 | 171 us: 1.16x slower                                                                                         |
| sympy_str                        | 103 ms                                                                                                 | 120 ms: 1.17x slower                                                                                         |
| django_template                  | 15.7 ms                                                                                                | 18.4 ms: 1.17x slower                                                                                        |
| fannkuch                         | 191 ms                                                                                                 | 225 ms: 1.18x slower                                                                                         |
| sympy_expand                     | 172 ms                                                                                                 | 203 ms: 1.18x slower                                                                                         |
| sqlglot_transpile                | 697 us                                                                                                 | 825 us: 1.18x slower                                                                                         |
| chaos                            | 28.4 ms                                                                                                | 33.7 ms: 1.19x slower                                                                                        |
| deepcopy                         | 109 us                                                                                                 | 130 us: 1.19x slower                                                                                         |
| logging_simple                   | 2.42 us                                                                                                | 2.87 us: 1.19x slower                                                                                        |
| logging_format                   | 2.63 us                                                                                                | 3.13 us: 1.19x slower                                                                                        |
| richards                         | 22.9 ms                                                                                                | 27.3 ms: 1.19x slower                                                                                        |
| typing_runtime_protocols         | 67.7 us                                                                                                | 80.7 us: 1.19x slower                                                                                        |
| generators                       | 18.5 ms                                                                                                | 22.1 ms: 1.19x slower                                                                                        |
| sqlglot_parse                    | 575 us                                                                                                 | 688 us: 1.20x slower                                                                                         |
| genshi_xml                       | 21.8 ms                                                                                                | 26.1 ms: 1.20x slower                                                                                        |
| coverage                         | 32.0 ms                                                                                                | 38.4 ms: 1.20x slower                                                                                        |
| spectral_norm                    | 49.2 ms                                                                                                | 59.5 ms: 1.21x slower                                                                                        |
| meteor_contest                   | 49.5 ms                                                                                                | 59.9 ms: 1.21x slower                                                                                        |
| regex_compile                    | 49.0 ms                                                                                                | 59.5 ms: 1.21x slower                                                                                        |
| deepcopy_reduce                  | 1.15 us                                                                                                | 1.40 us: 1.22x slower                                                                                        |
| unpickle_pure_python             | 105 us                                                                                                 | 128 us: 1.22x slower                                                                                         |
| genshi_text                      | 10.6 ms                                                                                                | 13.0 ms: 1.23x slower                                                                                        |
| richards_super                   | 25.5 ms                                                                                                | 31.4 ms: 1.23x slower                                                                                        |
| scimark_fft                      | 132 ms                                                                                                 | 163 ms: 1.23x slower                                                                                         |
| tomli_loads                      | 862 ms                                                                                                 | 1.07 sec: 1.25x slower                                                                                       |
| deltablue                        | 1.60 ms                                                                                                | 2.00 ms: 1.25x slower                                                                                        |
| pprint_safe_repr                 | 329 ms                                                                                                 | 412 ms: 1.25x slower                                                                                         |
| pprint_pformat                   | 666 ms                                                                                                 | 839 ms: 1.26x slower                                                                                         |
| go                               | 58.9 ms                                                                                                | 74.6 ms: 1.27x slower                                                                                        |
| scimark_sor                      | 54.9 ms                                                                                                | 69.8 ms: 1.27x slower                                                                                        |
| raytrace                         | 125 ms                                                                                                 | 159 ms: 1.28x slower                                                                                         |
| logging_silent                   | 43.8 ns                                                                                                | 56.1 ns: 1.28x slower                                                                                        |
| mako                             | 4.82 ms                                                                                                | 6.19 ms: 1.29x slower                                                                                        |
| scimark_monte_carlo              | 31.3 ms                                                                                                | 40.3 ms: 1.29x slower                                                                                        |
| async_tree_eager                 | 43.8 ms                                                                                                | 56.9 ms: 1.30x slower                                                                                        |
| comprehensions                   | 7.79 us                                                                                                | 10.2 us: 1.31x slower                                                                                        |
| scimark_sparse_mat_mult          | 1.87 ms                                                                                                | 2.48 ms: 1.32x slower                                                                                        |
| hexiom                           | 3.00 ms                                                                                                | 3.98 ms: 1.33x slower                                                                                        |
| deepcopy_memo                    | 12.9 us                                                                                                | 17.2 us: 1.34x slower                                                                                        |
| scimark_lu                       | 49.9 ms                                                                                                | 67.1 ms: 1.35x slower                                                                                        |
| bench_thread_pool                | 432 us                                                                                                 | 613 us: 1.42x slower                                                                                         |
| nbody                            | 51.0 ms                                                                                                | 77.9 ms: 1.53x slower                                                                                        |
| Geometric mean                   | (ref)                                                                                                  | 1.09x slower                                                                                                 |
Ignored benchmarks (1) of results/bm-20250314-3.14.0a6-77b2c93/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93.json: dask

- Geometric mean (including insignificant results): 1.082x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.10x