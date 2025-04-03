# Results vs. base

- fork: python
- ref: b3e3cc054c2c7718c0ad
- machine: darwin-arm64
- commit hash: b3e3cc0
- commit date: 2025-04-02
- overall geometric mean: 1.055x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 128 ms                                                                   | 122 ms: 1.05x faster                                                     |
| docutils       | 1.04 sec                                                                 | 1.01 sec: 1.02x faster                                                   |
| html5lib       | 23.4 ms                                                                  | 23.6 ms: 1.01x slower                                                    |
| sphinx         | 434 ms                                                                   | 425 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none_tg               | 95.5 ms                                                                  | 88.2 ms: 1.08x faster                                                    |
| async_tree_io_tg                 | 216 ms                                                                   | 200 ms: 1.08x faster                                                     |
| async_tree_io                    | 231 ms                                                                   | 214 ms: 1.08x faster                                                     |
| async_tree_eager_io_tg           | 214 ms                                                                   | 199 ms: 1.07x faster                                                     |
| async_tree_none                  | 110 ms                                                                   | 103 ms: 1.07x faster                                                     |
| async_tree_eager_io              | 225 ms                                                                   | 210 ms: 1.07x faster                                                     |
| async_tree_eager_tg              | 84.2 ms                                                                  | 79.2 ms: 1.06x faster                                                    |
| coroutines                       | 11.2 ms                                                                  | 10.6 ms: 1.06x faster                                                    |
| async_generators                 | 190 ms                                                                   | 181 ms: 1.05x faster                                                     |
| async_tree_memoization           | 139 ms                                                                   | 133 ms: 1.05x faster                                                     |
| async_tree_eager                 | 53.6 ms                                                                  | 51.2 ms: 1.05x faster                                                    |
| async_tree_memoization_tg        | 131 ms                                                                   | 126 ms: 1.04x faster                                                     |
| async_tree_eager_memoization_tg  | 117 ms                                                                   | 114 ms: 1.03x faster                                                     |
| async_tree_eager_memoization     | 115 ms                                                                   | 113 ms: 1.02x faster                                                     |
| async_tree_cpu_io_mixed          | 249 ms                                                                   | 244 ms: 1.02x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 239 ms                                                                   | 235 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 228 ms                                                                   | 225 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                                   | 223 ms: 1.01x faster                                                     |
| asyncio_websockets               | 188 ms                                                                   | 189 ms: 1.00x slower                                                     |
| Geometric mean                   | (ref)                                                                    | 1.05x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.6 ms                                                                  | 28.4 ms: 1.11x faster                                                    |
| nbody          | 58.8 ms                                                                  | 54.3 ms: 1.08x faster                                                    |
| pidigits       | 159 ms                                                                   | 165 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 56.7 ms                                                                  | 53.8 ms: 1.05x faster                                                    |
| regex_v8       | 9.58 ms                                                                  | 10.00 ms: 1.04x slower                                                   |
| regex_effbot   | 1.38 ms                                                                  | 1.50 ms: 1.08x slower                                                    |
| regex_dna      | 91.2 ms                                                                  | 101 ms: 1.11x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.05x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle_pure_python | 124 us                                                                   | 108 us: 1.15x faster                                                     |
| xml_etree_iterparse  | 41.5 ms                                                                  | 36.7 ms: 1.13x faster                                                    |
| xml_etree_process    | 29.8 ms                                                                  | 26.9 ms: 1.11x faster                                                    |
| xml_etree_generate   | 40.2 ms                                                                  | 36.9 ms: 1.09x faster                                                    |
| pickle_pure_python   | 163 us                                                                   | 153 us: 1.07x faster                                                     |
| tomli_loads          | 1.02 sec                                                                 | 976 ms: 1.05x faster                                                     |
| xml_etree_parse      | 58.2 ms                                                                  | 56.1 ms: 1.04x faster                                                    |
| json_dumps           | 5.09 ms                                                                  | 5.06 ms: 1.01x faster                                                    |
| json_loads           | 11.6 us                                                                  | 12.0 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 9.19 ms                                                                  | 9.53 ms: 1.04x slower                                                    |
| python_startup_no_site | 7.24 ms                                                                  | 7.58 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                                    | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|-----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 26.1 ms                                                                  | 23.6 ms: 1.11x faster                                                    |
| genshi_text     | 12.4 ms                                                                  | 11.5 ms: 1.09x faster                                                    |
| mako            | 6.00 ms                                                                  | 5.58 ms: 1.08x faster                                                    |
| django_template | 17.6 ms                                                                  | 17.0 ms: 1.04x faster                                                    |
| Geometric mean  | (ref)                                                                    | 1.08x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| generators                       | 23.4 ms                                                                  | 19.1 ms: 1.23x faster                                                    |
| gc_traversal                     | 920 us                                                                   | 758 us: 1.21x faster                                                     |
| scimark_sor                      | 66.6 ms                                                                  | 55.4 ms: 1.20x faster                                                    |
| hexiom                           | 3.76 ms                                                                  | 3.18 ms: 1.18x faster                                                    |
| unpickle_pure_python             | 124 us                                                                   | 108 us: 1.15x faster                                                     |
| deltablue                        | 1.88 ms                                                                  | 1.65 ms: 1.14x faster                                                    |
| xml_etree_iterparse              | 41.5 ms                                                                  | 36.7 ms: 1.13x faster                                                    |
| nqueens                          | 47.9 ms                                                                  | 42.5 ms: 1.13x faster                                                    |
| scimark_monte_carlo              | 37.6 ms                                                                  | 33.4 ms: 1.12x faster                                                    |
| scimark_lu                       | 61.6 ms                                                                  | 54.9 ms: 1.12x faster                                                    |
| raytrace                         | 148 ms                                                                   | 132 ms: 1.12x faster                                                     |
| spectral_norm                    | 57.4 ms                                                                  | 51.3 ms: 1.12x faster                                                    |
| float                            | 31.6 ms                                                                  | 28.4 ms: 1.11x faster                                                    |
| comprehensions                   | 9.70 us                                                                  | 8.74 us: 1.11x faster                                                    |
| xml_etree_process                | 29.8 ms                                                                  | 26.9 ms: 1.11x faster                                                    |
| genshi_xml                       | 26.1 ms                                                                  | 23.6 ms: 1.11x faster                                                    |
| pyflate                          | 221 ms                                                                   | 200 ms: 1.11x faster                                                     |
| mdp                              | 626 ms                                                                   | 571 ms: 1.10x faster                                                     |
| crypto_pyaes                     | 45.3 ms                                                                  | 41.4 ms: 1.09x faster                                                    |
| deepcopy_memo                    | 15.8 us                                                                  | 14.5 us: 1.09x faster                                                    |
| xml_etree_generate               | 40.2 ms                                                                  | 36.9 ms: 1.09x faster                                                    |
| genshi_text                      | 12.4 ms                                                                  | 11.5 ms: 1.09x faster                                                    |
| fannkuch                         | 209 ms                                                                   | 193 ms: 1.09x faster                                                     |
| bpe_tokeniser                    | 2.14 sec                                                                 | 1.98 sec: 1.08x faster                                                   |
| nbody                            | 58.8 ms                                                                  | 54.3 ms: 1.08x faster                                                    |
| async_tree_none_tg               | 95.5 ms                                                                  | 88.2 ms: 1.08x faster                                                    |
| create_gc_cycles                 | 497 us                                                                   | 459 us: 1.08x faster                                                     |
| go                               | 68.8 ms                                                                  | 63.5 ms: 1.08x faster                                                    |
| typing_runtime_protocols         | 78.9 us                                                                  | 72.9 us: 1.08x faster                                                    |
| async_tree_io_tg                 | 216 ms                                                                   | 200 ms: 1.08x faster                                                     |
| async_tree_io                    | 231 ms                                                                   | 214 ms: 1.08x faster                                                     |
| richards                         | 26.7 ms                                                                  | 24.8 ms: 1.08x faster                                                    |
| mako                             | 6.00 ms                                                                  | 5.58 ms: 1.08x faster                                                    |
| richards_super                   | 30.4 ms                                                                  | 28.3 ms: 1.07x faster                                                    |
| async_tree_eager_io_tg           | 214 ms                                                                   | 199 ms: 1.07x faster                                                     |
| async_tree_none                  | 110 ms                                                                   | 103 ms: 1.07x faster                                                     |
| pprint_safe_repr                 | 395 ms                                                                   | 369 ms: 1.07x faster                                                     |
| async_tree_eager_io              | 225 ms                                                                   | 210 ms: 1.07x faster                                                     |
| pprint_pformat                   | 802 ms                                                                   | 752 ms: 1.07x faster                                                     |
| pickle_pure_python               | 163 us                                                                   | 153 us: 1.07x faster                                                     |
| sqlglot_v2_parse                 | 647 us                                                                   | 608 us: 1.06x faster                                                     |
| async_tree_eager_tg              | 84.2 ms                                                                  | 79.2 ms: 1.06x faster                                                    |
| coverage                         | 41.3 ms                                                                  | 38.8 ms: 1.06x faster                                                    |
| coroutines                       | 11.2 ms                                                                  | 10.6 ms: 1.06x faster                                                    |
| logging_silent                   | 52.2 ns                                                                  | 49.2 ns: 1.06x faster                                                    |
| logging_simple                   | 2.76 us                                                                  | 2.60 us: 1.06x faster                                                    |
| logging_format                   | 3.05 us                                                                  | 2.87 us: 1.06x faster                                                    |
| sqlglot_v2_transpile             | 776 us                                                                   | 733 us: 1.06x faster                                                     |
| sqlglot_v2_normalize             | 53.2 ms                                                                  | 50.2 ms: 1.06x faster                                                    |
| scimark_fft                      | 149 ms                                                                   | 141 ms: 1.06x faster                                                     |
| shortest_path                    | 244 ms                                                                   | 231 ms: 1.06x faster                                                     |
| regex_compile                    | 56.7 ms                                                                  | 53.8 ms: 1.05x faster                                                    |
| connected_components             | 231 ms                                                                   | 219 ms: 1.05x faster                                                     |
| async_generators                 | 190 ms                                                                   | 181 ms: 1.05x faster                                                     |
| 2to3                             | 128 ms                                                                   | 122 ms: 1.05x faster                                                     |
| pathlib                          | 11.6 ms                                                                  | 11.1 ms: 1.05x faster                                                    |
| async_tree_memoization           | 139 ms                                                                   | 133 ms: 1.05x faster                                                     |
| scimark_sparse_mat_mult          | 2.23 ms                                                                  | 2.13 ms: 1.05x faster                                                    |
| tomli_loads                      | 1.02 sec                                                                 | 976 ms: 1.05x faster                                                     |
| sympy_str                        | 117 ms                                                                   | 112 ms: 1.05x faster                                                     |
| sympy_integrate                  | 8.60 ms                                                                  | 8.22 ms: 1.05x faster                                                    |
| async_tree_eager                 | 53.6 ms                                                                  | 51.2 ms: 1.05x faster                                                    |
| sympy_expand                     | 199 ms                                                                   | 191 ms: 1.04x faster                                                     |
| k_core                           | 1.02 sec                                                                 | 981 ms: 1.04x faster                                                     |
| chaos                            | 30.7 ms                                                                  | 29.5 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 58.2 ms                                                                  | 56.1 ms: 1.04x faster                                                    |
| sqlglot_v2_optimize              | 25.7 ms                                                                  | 24.8 ms: 1.04x faster                                                    |
| django_template                  | 17.6 ms                                                                  | 17.0 ms: 1.04x faster                                                    |
| async_tree_memoization_tg        | 131 ms                                                                   | 126 ms: 1.04x faster                                                     |
| async_tree_eager_memoization_tg  | 117 ms                                                                   | 114 ms: 1.03x faster                                                     |
| pycparser                        | 488 ms                                                                   | 473 ms: 1.03x faster                                                     |
| pylint                           | 123 ms                                                                   | 120 ms: 1.03x faster                                                     |
| deepcopy_reduce                  | 1.33 us                                                                  | 1.29 us: 1.03x faster                                                    |
| bench_thread_pool                | 591 us                                                                   | 578 us: 1.02x faster                                                     |
| sphinx                           | 434 ms                                                                   | 425 ms: 1.02x faster                                                     |
| docutils                         | 1.04 sec                                                                 | 1.01 sec: 1.02x faster                                                   |
| sqlite_synth                     | 835 ns                                                                   | 817 ns: 1.02x faster                                                     |
| async_tree_eager_memoization     | 115 ms                                                                   | 113 ms: 1.02x faster                                                     |
| async_tree_cpu_io_mixed          | 249 ms                                                                   | 244 ms: 1.02x faster                                                     |
| subparsers                       | 9.07 ms                                                                  | 8.90 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 239 ms                                                                   | 235 ms: 1.02x faster                                                     |
| telco                            | 3.46 ms                                                                  | 3.41 ms: 1.01x faster                                                    |
| sympy_sum                        | 62.9 ms                                                                  | 62.3 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 228 ms                                                                   | 225 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                                   | 223 ms: 1.01x faster                                                     |
| json_dumps                       | 5.09 ms                                                                  | 5.06 ms: 1.01x faster                                                    |
| many_optionals                   | 247 us                                                                   | 246 us: 1.01x faster                                                     |
| meteor_contest                   | 57.4 ms                                                                  | 57.1 ms: 1.01x faster                                                    |
| sqlalchemy_imperative            | 5.80 ms                                                                  | 5.77 ms: 1.00x faster                                                    |
| asyncio_websockets               | 188 ms                                                                   | 189 ms: 1.00x slower                                                     |
| sqlalchemy_declarative           | 50.4 ms                                                                  | 50.8 ms: 1.01x slower                                                    |
| html5lib                         | 23.4 ms                                                                  | 23.6 ms: 1.01x slower                                                    |
| deepcopy                         | 122 us                                                                   | 125 us: 1.03x slower                                                     |
| json_loads                       | 11.6 us                                                                  | 12.0 us: 1.03x slower                                                    |
| pidigits                         | 159 ms                                                                   | 165 ms: 1.03x slower                                                     |
| python_startup                   | 9.19 ms                                                                  | 9.53 ms: 1.04x slower                                                    |
| regex_v8                         | 9.58 ms                                                                  | 10.00 ms: 1.04x slower                                                   |
| python_startup_no_site           | 7.24 ms                                                                  | 7.58 ms: 1.05x slower                                                    |
| bench_mp_pool                    | 39.2 ms                                                                  | 42.1 ms: 1.07x slower                                                    |
| regex_effbot                     | 1.38 ms                                                                  | 1.50 ms: 1.08x slower                                                    |
| regex_dna                        | 91.2 ms                                                                  | 101 ms: 1.11x slower                                                     |
| Geometric mean                   | (ref)                                                                    | 1.05x faster                                                             |

Benchmark hidden because not significant (2): dulwich_log, json

- Geometric mean (including insignificant results): 1.055x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.01x