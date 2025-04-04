# Results vs. default_base_vs_NOGIL

- fork: tom-pytel
- ref: 579bd08e9f4db18fbbe0
- machine: darwin-arm64
- commit hash: 579bd08
- commit date: 2025-03-30
- overall geometric mean: 1.010x slower
- HPT reliability: 99.13%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 116 ms                                                                   | 122 ms: 1.05x slower                                                          |
| docutils       | 1.07 sec                                                                 | 1.00 sec: 1.06x faster                                                        |
| html5lib       | 24.5 ms                                                                  | 24.1 ms: 1.02x faster                                                         |
| sphinx         | 419 ms                                                                   | 425 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 261 ms                                                                   | 201 ms: 1.30x faster                                                          |
| async_tree_io_tg                 | 261 ms                                                                   | 202 ms: 1.29x faster                                                          |
| async_tree_io                    | 271 ms                                                                   | 218 ms: 1.25x faster                                                          |
| async_tree_none_tg               | 110 ms                                                                   | 89.0 ms: 1.23x faster                                                         |
| async_tree_eager_io              | 262 ms                                                                   | 213 ms: 1.23x faster                                                          |
| async_tree_memoization_tg        | 151 ms                                                                   | 126 ms: 1.19x faster                                                          |
| async_tree_eager_memoization_tg  | 135 ms                                                                   | 115 ms: 1.17x faster                                                          |
| async_tree_cpu_io_mixed_tg       | 268 ms                                                                   | 233 ms: 1.15x faster                                                          |
| async_tree_memoization           | 153 ms                                                                   | 134 ms: 1.14x faster                                                          |
| async_tree_eager_tg              | 91.0 ms                                                                  | 79.9 ms: 1.14x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 248 ms                                                                   | 224 ms: 1.11x faster                                                          |
| async_tree_cpu_io_mixed          | 266 ms                                                                   | 242 ms: 1.10x faster                                                          |
| async_tree_none                  | 114 ms                                                                   | 105 ms: 1.09x faster                                                          |
| asyncio_websockets               | 193 ms                                                                   | 187 ms: 1.03x faster                                                          |
| coroutines                       | 10.7 ms                                                                  | 10.6 ms: 1.01x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 223 ms                                                                   | 222 ms: 1.00x faster                                                          |
| async_generators                 | 175 ms                                                                   | 178 ms: 1.01x slower                                                          |
| async_tree_eager                 | 43.4 ms                                                                  | 51.8 ms: 1.19x slower                                                         |
| Geometric mean                   | (ref)                                                                    | 1.11x faster                                                                  |

Benchmark hidden because not significant (1): async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 167 ms                                                                   | 162 ms: 1.03x faster                                                          |
| float          | 32.0 ms                                                                  | 32.3 ms: 1.01x slower                                                         |
| nbody          | 51.2 ms                                                                  | 61.3 ms: 1.20x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.06x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_v8       | 10.4 ms                                                                  | 10.2 ms: 1.02x faster                                                         |
| regex_dna      | 100 ms                                                                   | 103 ms: 1.02x slower                                                          |
| regex_effbot   | 1.49 ms                                                                  | 1.56 ms: 1.05x slower                                                         |
| regex_compile  | 50.2 ms                                                                  | 55.6 ms: 1.11x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.04x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| xml_etree_iterparse  | 45.8 ms                                                                  | 36.4 ms: 1.26x faster                                                         |
| xml_etree_parse      | 64.3 ms                                                                  | 57.2 ms: 1.12x faster                                                         |
| json_dumps           | 5.08 ms                                                                  | 5.12 ms: 1.01x slower                                                         |
| xml_etree_generate   | 37.0 ms                                                                  | 37.5 ms: 1.01x slower                                                         |
| json_loads           | 11.7 us                                                                  | 12.0 us: 1.02x slower                                                         |
| xml_etree_process    | 26.4 ms                                                                  | 27.5 ms: 1.04x slower                                                         |
| pickle_pure_python   | 151 us                                                                   | 159 us: 1.05x slower                                                          |
| unpickle_pure_python | 105 us                                                                   | 112 us: 1.06x slower                                                          |
| tomli_loads          | 936 ms                                                                   | 1.00 sec: 1.07x slower                                                        |
| Geometric mean       | (ref)                                                                    | 1.01x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 9.04 ms                                                                  | 9.48 ms: 1.05x slower                                                         |
| python_startup_no_site | 6.77 ms                                                                  | 7.60 ms: 1.12x slower                                                         |
| Geometric mean         | (ref)                                                                    | 1.08x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| django_template | 15.8 ms                                                                  | 16.9 ms: 1.07x slower                                                         |
| genshi_xml      | 22.6 ms                                                                  | 24.5 ms: 1.09x slower                                                         |
| genshi_text     | 10.5 ms                                                                  | 11.9 ms: 1.13x slower                                                         |
| mako            | 4.85 ms                                                                  | 5.80 ms: 1.20x slower                                                         |
| Geometric mean  | (ref)                                                                    | 1.12x slower                                                                  |

All benchmarks:
===============

| Benchmark                        | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| gc_traversal                     | 2.05 ms                                                                  | 760 us: 2.70x faster                                                          |
| create_gc_cycles                 | 904 us                                                                   | 461 us: 1.96x faster                                                          |
| async_tree_eager_io_tg           | 261 ms                                                                   | 201 ms: 1.30x faster                                                          |
| async_tree_io_tg                 | 261 ms                                                                   | 202 ms: 1.29x faster                                                          |
| xml_etree_iterparse              | 45.8 ms                                                                  | 36.4 ms: 1.26x faster                                                         |
| async_tree_io                    | 271 ms                                                                   | 218 ms: 1.25x faster                                                          |
| async_tree_none_tg               | 110 ms                                                                   | 89.0 ms: 1.23x faster                                                         |
| async_tree_eager_io              | 262 ms                                                                   | 213 ms: 1.23x faster                                                          |
| async_tree_memoization_tg        | 151 ms                                                                   | 126 ms: 1.19x faster                                                          |
| async_tree_eager_memoization_tg  | 135 ms                                                                   | 115 ms: 1.17x faster                                                          |
| sqlite_synth                     | 957 ns                                                                   | 824 ns: 1.16x faster                                                          |
| async_tree_cpu_io_mixed_tg       | 268 ms                                                                   | 233 ms: 1.15x faster                                                          |
| async_tree_memoization           | 153 ms                                                                   | 134 ms: 1.14x faster                                                          |
| async_tree_eager_tg              | 91.0 ms                                                                  | 79.9 ms: 1.14x faster                                                         |
| xml_etree_parse                  | 64.3 ms                                                                  | 57.2 ms: 1.12x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 248 ms                                                                   | 224 ms: 1.11x faster                                                          |
| async_tree_cpu_io_mixed          | 266 ms                                                                   | 242 ms: 1.10x faster                                                          |
| async_tree_none                  | 114 ms                                                                   | 105 ms: 1.09x faster                                                          |
| docutils                         | 1.07 sec                                                                 | 1.00 sec: 1.06x faster                                                        |
| pycparser                        | 500 ms                                                                   | 482 ms: 1.04x faster                                                          |
| asyncio_websockets               | 193 ms                                                                   | 187 ms: 1.03x faster                                                          |
| pidigits                         | 167 ms                                                                   | 162 ms: 1.03x faster                                                          |
| html5lib                         | 24.5 ms                                                                  | 24.1 ms: 1.02x faster                                                         |
| regex_v8                         | 10.4 ms                                                                  | 10.2 ms: 1.02x faster                                                         |
| pathlib                          | 11.2 ms                                                                  | 11.1 ms: 1.01x faster                                                         |
| subparsers                       | 9.04 ms                                                                  | 8.96 ms: 1.01x faster                                                         |
| coroutines                       | 10.7 ms                                                                  | 10.6 ms: 1.01x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 223 ms                                                                   | 222 ms: 1.00x faster                                                          |
| bpe_tokeniser                    | 2.04 sec                                                                 | 2.05 sec: 1.01x slower                                                        |
| float                            | 32.0 ms                                                                  | 32.3 ms: 1.01x slower                                                         |
| json_dumps                       | 5.08 ms                                                                  | 5.12 ms: 1.01x slower                                                         |
| xml_etree_generate               | 37.0 ms                                                                  | 37.5 ms: 1.01x slower                                                         |
| pyflate                          | 210 ms                                                                   | 213 ms: 1.01x slower                                                          |
| many_optionals                   | 241 us                                                                   | 244 us: 1.01x slower                                                          |
| async_generators                 | 175 ms                                                                   | 178 ms: 1.01x slower                                                          |
| sphinx                           | 419 ms                                                                   | 425 ms: 1.01x slower                                                          |
| bench_mp_pool                    | 41.4 ms                                                                  | 42.0 ms: 1.02x slower                                                         |
| sqlglot_v2_normalize             | 48.2 ms                                                                  | 49.0 ms: 1.02x slower                                                         |
| json_loads                       | 11.7 us                                                                  | 12.0 us: 1.02x slower                                                         |
| regex_dna                        | 100 ms                                                                   | 103 ms: 1.02x slower                                                          |
| generators                       | 18.3 ms                                                                  | 18.8 ms: 1.03x slower                                                         |
| nqueens                          | 41.7 ms                                                                  | 42.9 ms: 1.03x slower                                                         |
| pylint                           | 116 ms                                                                   | 119 ms: 1.03x slower                                                          |
| sqlglot_v2_optimize              | 23.7 ms                                                                  | 24.5 ms: 1.03x slower                                                         |
| xml_etree_process                | 26.4 ms                                                                  | 27.5 ms: 1.04x slower                                                         |
| dulwich_log                      | 18.1 ms                                                                  | 18.9 ms: 1.04x slower                                                         |
| regex_effbot                     | 1.49 ms                                                                  | 1.56 ms: 1.05x slower                                                         |
| python_startup                   | 9.04 ms                                                                  | 9.48 ms: 1.05x slower                                                         |
| pickle_pure_python               | 151 us                                                                   | 159 us: 1.05x slower                                                          |
| 2to3                             | 116 ms                                                                   | 122 ms: 1.05x slower                                                          |
| mdp                              | 1.08 sec                                                                 | 1.14 sec: 1.05x slower                                                        |
| k_core                           | 963 ms                                                                   | 1.02 sec: 1.06x slower                                                        |
| shortest_path                    | 221 ms                                                                   | 234 ms: 1.06x slower                                                          |
| fannkuch                         | 192 ms                                                                   | 203 ms: 1.06x slower                                                          |
| unpickle_pure_python             | 105 us                                                                   | 112 us: 1.06x slower                                                          |
| sqlalchemy_imperative            | 5.44 ms                                                                  | 5.79 ms: 1.06x slower                                                         |
| crypto_pyaes                     | 38.5 ms                                                                  | 41.0 ms: 1.06x slower                                                         |
| django_template                  | 15.8 ms                                                                  | 16.9 ms: 1.07x slower                                                         |
| tomli_loads                      | 936 ms                                                                   | 1.00 sec: 1.07x slower                                                        |
| sympy_integrate                  | 7.77 ms                                                                  | 8.34 ms: 1.07x slower                                                         |
| sympy_sum                        | 57.1 ms                                                                  | 61.4 ms: 1.08x slower                                                         |
| telco                            | 3.13 ms                                                                  | 3.37 ms: 1.08x slower                                                         |
| chaos                            | 28.7 ms                                                                  | 30.9 ms: 1.08x slower                                                         |
| thrift                           | 315 us                                                                   | 340 us: 1.08x slower                                                          |
| go                               | 61.9 ms                                                                  | 67.1 ms: 1.08x slower                                                         |
| logging_format                   | 2.72 us                                                                  | 2.95 us: 1.08x slower                                                         |
| raytrace                         | 129 ms                                                                   | 140 ms: 1.08x slower                                                          |
| genshi_xml                       | 22.6 ms                                                                  | 24.5 ms: 1.09x slower                                                         |
| deltablue                        | 1.59 ms                                                                  | 1.73 ms: 1.09x slower                                                         |
| connected_components             | 204 ms                                                                   | 222 ms: 1.09x slower                                                          |
| scimark_sor                      | 53.2 ms                                                                  | 57.9 ms: 1.09x slower                                                         |
| deepcopy_reduce                  | 1.20 us                                                                  | 1.30 us: 1.09x slower                                                         |
| logging_simple                   | 2.47 us                                                                  | 2.69 us: 1.09x slower                                                         |
| sqlglot_v2_transpile             | 699 us                                                                   | 768 us: 1.10x slower                                                          |
| sympy_str                        | 102 ms                                                                   | 112 ms: 1.10x slower                                                          |
| sqlglot_v2_parse                 | 576 us                                                                   | 636 us: 1.10x slower                                                          |
| sqlalchemy_declarative           | 45.9 ms                                                                  | 50.8 ms: 1.11x slower                                                         |
| sympy_expand                     | 172 ms                                                                   | 191 ms: 1.11x slower                                                          |
| regex_compile                    | 50.2 ms                                                                  | 55.6 ms: 1.11x slower                                                         |
| deepcopy                         | 114 us                                                                   | 127 us: 1.11x slower                                                          |
| meteor_contest                   | 50.9 ms                                                                  | 56.6 ms: 1.11x slower                                                         |
| scimark_sparse_mat_mult          | 2.00 ms                                                                  | 2.23 ms: 1.12x slower                                                         |
| spectral_norm                    | 46.9 ms                                                                  | 52.3 ms: 1.12x slower                                                         |
| hexiom                           | 2.96 ms                                                                  | 3.31 ms: 1.12x slower                                                         |
| python_startup_no_site           | 6.77 ms                                                                  | 7.60 ms: 1.12x slower                                                         |
| scimark_fft                      | 132 ms                                                                   | 149 ms: 1.13x slower                                                          |
| richards                         | 22.6 ms                                                                  | 25.5 ms: 1.13x slower                                                         |
| genshi_text                      | 10.5 ms                                                                  | 11.9 ms: 1.13x slower                                                         |
| comprehensions                   | 7.77 us                                                                  | 8.85 us: 1.14x slower                                                         |
| richards_super                   | 25.4 ms                                                                  | 28.9 ms: 1.14x slower                                                         |
| typing_runtime_protocols         | 65.4 us                                                                  | 74.6 us: 1.14x slower                                                         |
| logging_silent                   | 42.9 ns                                                                  | 49.1 ns: 1.14x slower                                                         |
| pprint_safe_repr                 | 335 ms                                                                   | 386 ms: 1.15x slower                                                          |
| pprint_pformat                   | 681 ms                                                                   | 784 ms: 1.15x slower                                                          |
| scimark_monte_carlo              | 30.5 ms                                                                  | 35.3 ms: 1.16x slower                                                         |
| scimark_lu                       | 47.2 ms                                                                  | 55.5 ms: 1.18x slower                                                         |
| async_tree_eager                 | 43.4 ms                                                                  | 51.8 ms: 1.19x slower                                                         |
| coverage                         | 32.7 ms                                                                  | 39.1 ms: 1.20x slower                                                         |
| mako                             | 4.85 ms                                                                  | 5.80 ms: 1.20x slower                                                         |
| deepcopy_memo                    | 12.9 us                                                                  | 15.5 us: 1.20x slower                                                         |
| nbody                            | 51.2 ms                                                                  | 61.3 ms: 1.20x slower                                                         |
| bench_thread_pool                | 433 us                                                                   | 587 us: 1.35x slower                                                          |
| Geometric mean                   | (ref)                                                                    | 1.02x slower                                                                  |

Benchmark hidden because not significant (2): json, async_tree_eager_memoization
Ignored benchmarks (1) of results/bm-20250325-3.14.0a6+-96ef4c5/bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5.json: dask

- Geometric mean (including insignificant results): 1.010x slower

# HPT report

- Reliability score: 99.13% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.11x