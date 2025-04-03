# Results vs. default_base_vs_NOGIL

- fork: python
- ref: b3e3cc054c2c7718c0ad
- machine: darwin-arm64
- commit hash: b3e3cc0
- commit date: 2025-04-02
- overall geometric mean: 1.030x faster
- HPT reliability: 85.17%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 115 ms                                                                   | 122 ms: 1.06x slower                                                     |
| docutils       | 1.08 sec                                                                 | 1.01 sec: 1.06x faster                                                   |
| html5lib       | 23.3 ms                                                                  | 23.6 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 265 ms                                                                   | 199 ms: 1.33x faster                                                     |
| async_tree_io_tg                 | 264 ms                                                                   | 200 ms: 1.31x faster                                                     |
| async_tree_none_tg               | 110 ms                                                                   | 88.2 ms: 1.25x faster                                                    |
| async_tree_eager_io              | 262 ms                                                                   | 210 ms: 1.25x faster                                                     |
| async_tree_io                    | 264 ms                                                                   | 214 ms: 1.23x faster                                                     |
| async_tree_memoization_tg        | 151 ms                                                                   | 126 ms: 1.19x faster                                                     |
| async_tree_eager_memoization_tg  | 135 ms                                                                   | 114 ms: 1.18x faster                                                     |
| async_tree_eager_tg              | 92.3 ms                                                                  | 79.2 ms: 1.17x faster                                                    |
| async_tree_none                  | 119 ms                                                                   | 103 ms: 1.15x faster                                                     |
| async_tree_memoization           | 152 ms                                                                   | 133 ms: 1.14x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 262 ms                                                                   | 235 ms: 1.12x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 248 ms                                                                   | 225 ms: 1.10x faster                                                     |
| coroutines                       | 11.5 ms                                                                  | 10.6 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 264 ms                                                                   | 244 ms: 1.08x faster                                                     |
| async_tree_eager_memoization     | 115 ms                                                                   | 113 ms: 1.02x faster                                                     |
| asyncio_websockets               | 191 ms                                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 222 ms                                                                   | 223 ms: 1.00x slower                                                     |
| async_generators                 | 178 ms                                                                   | 181 ms: 1.02x slower                                                     |
| async_tree_eager                 | 45.7 ms                                                                  | 51.2 ms: 1.12x slower                                                    |
| Geometric mean                   | (ref)                                                                    | 1.13x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 33.1 ms                                                                  | 28.4 ms: 1.17x faster                                                    |
| pidigits       | 161 ms                                                                   | 165 ms: 1.02x slower                                                     |
| nbody          | 52.8 ms                                                                  | 54.3 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.1 ms                                                                  | 10.00 ms: 1.01x faster                                                   |
| regex_effbot   | 1.43 ms                                                                  | 1.50 ms: 1.05x slower                                                    |
| regex_compile  | 50.3 ms                                                                  | 53.8 ms: 1.07x slower                                                    |
| regex_dna      | 92.5 ms                                                                  | 101 ms: 1.10x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.05x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 47.9 ms                                                                  | 36.7 ms: 1.31x faster                                                    |
| xml_etree_parse      | 62.7 ms                                                                  | 56.1 ms: 1.12x faster                                                    |
| unpickle_pure_python | 112 us                                                                   | 108 us: 1.04x faster                                                     |
| xml_etree_generate   | 38.1 ms                                                                  | 36.9 ms: 1.03x faster                                                    |
| xml_etree_process    | 27.7 ms                                                                  | 26.9 ms: 1.03x faster                                                    |
| json_dumps           | 5.12 ms                                                                  | 5.06 ms: 1.01x faster                                                    |
| pickle_pure_python   | 151 us                                                                   | 153 us: 1.01x slower                                                     |
| tomli_loads          | 949 ms                                                                   | 976 ms: 1.03x slower                                                     |
| json_loads           | 11.3 us                                                                  | 12.0 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                                    | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.70 ms                                                                  | 9.53 ms: 1.10x slower                                                    |
| python_startup_no_site | 6.46 ms                                                                  | 7.58 ms: 1.17x slower                                                    |
| Geometric mean         | (ref)                                                                    | 1.13x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|-----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 11.2 ms                                                                  | 11.5 ms: 1.02x slower                                                    |
| django_template | 16.6 ms                                                                  | 17.0 ms: 1.02x slower                                                    |
| genshi_xml      | 22.5 ms                                                                  | 23.6 ms: 1.05x slower                                                    |
| mako            | 5.06 ms                                                                  | 5.58 ms: 1.10x slower                                                    |
| Geometric mean  | (ref)                                                                    | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 |
|----------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.07 ms                                                                  | 758 us: 2.74x faster                                                     |
| create_gc_cycles                 | 886 us                                                                   | 459 us: 1.93x faster                                                     |
| async_tree_eager_io_tg           | 265 ms                                                                   | 199 ms: 1.33x faster                                                     |
| async_tree_io_tg                 | 264 ms                                                                   | 200 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 47.9 ms                                                                  | 36.7 ms: 1.31x faster                                                    |
| async_tree_none_tg               | 110 ms                                                                   | 88.2 ms: 1.25x faster                                                    |
| async_tree_eager_io              | 262 ms                                                                   | 210 ms: 1.25x faster                                                     |
| async_tree_io                    | 264 ms                                                                   | 214 ms: 1.23x faster                                                     |
| async_tree_memoization_tg        | 151 ms                                                                   | 126 ms: 1.19x faster                                                     |
| async_tree_eager_memoization_tg  | 135 ms                                                                   | 114 ms: 1.18x faster                                                     |
| sqlite_synth                     | 956 ns                                                                   | 817 ns: 1.17x faster                                                     |
| float                            | 33.1 ms                                                                  | 28.4 ms: 1.17x faster                                                    |
| async_tree_eager_tg              | 92.3 ms                                                                  | 79.2 ms: 1.17x faster                                                    |
| async_tree_none                  | 119 ms                                                                   | 103 ms: 1.15x faster                                                     |
| async_tree_memoization           | 152 ms                                                                   | 133 ms: 1.14x faster                                                     |
| scimark_sor                      | 62.7 ms                                                                  | 55.4 ms: 1.13x faster                                                    |
| xml_etree_parse                  | 62.7 ms                                                                  | 56.1 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 262 ms                                                                   | 235 ms: 1.12x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 248 ms                                                                   | 225 ms: 1.10x faster                                                     |
| coroutines                       | 11.5 ms                                                                  | 10.6 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 264 ms                                                                   | 244 ms: 1.08x faster                                                     |
| pyflate                          | 215 ms                                                                   | 200 ms: 1.08x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                                 | 1.98 sec: 1.08x faster                                                   |
| pycparser                        | 505 ms                                                                   | 473 ms: 1.07x faster                                                     |
| docutils                         | 1.08 sec                                                                 | 1.01 sec: 1.06x faster                                                   |
| pathlib                          | 11.6 ms                                                                  | 11.1 ms: 1.05x faster                                                    |
| nqueens                          | 44.6 ms                                                                  | 42.5 ms: 1.05x faster                                                    |
| spectral_norm                    | 53.5 ms                                                                  | 51.3 ms: 1.04x faster                                                    |
| unpickle_pure_python             | 112 us                                                                   | 108 us: 1.04x faster                                                     |
| scimark_lu                       | 57.1 ms                                                                  | 54.9 ms: 1.04x faster                                                    |
| scimark_fft                      | 146 ms                                                                   | 141 ms: 1.03x faster                                                     |
| fannkuch                         | 199 ms                                                                   | 193 ms: 1.03x faster                                                     |
| xml_etree_generate               | 38.1 ms                                                                  | 36.9 ms: 1.03x faster                                                    |
| xml_etree_process                | 27.7 ms                                                                  | 26.9 ms: 1.03x faster                                                    |
| async_tree_eager_memoization     | 115 ms                                                                   | 113 ms: 1.02x faster                                                     |
| deltablue                        | 1.68 ms                                                                  | 1.65 ms: 1.02x faster                                                    |
| hexiom                           | 3.23 ms                                                                  | 3.18 ms: 1.02x faster                                                    |
| asyncio_websockets               | 191 ms                                                                   | 189 ms: 1.01x faster                                                     |
| regex_v8                         | 10.1 ms                                                                  | 10.00 ms: 1.01x faster                                                   |
| sqlglot_v2_normalize             | 50.9 ms                                                                  | 50.2 ms: 1.01x faster                                                    |
| json_dumps                       | 5.12 ms                                                                  | 5.06 ms: 1.01x faster                                                    |
| crypto_pyaes                     | 41.5 ms                                                                  | 41.4 ms: 1.00x faster                                                    |
| pprint_safe_repr                 | 370 ms                                                                   | 369 ms: 1.00x faster                                                     |
| sqlglot_v2_optimize              | 24.7 ms                                                                  | 24.8 ms: 1.00x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 222 ms                                                                   | 223 ms: 1.00x slower                                                     |
| pickle_pure_python               | 151 us                                                                   | 153 us: 1.01x slower                                                     |
| pprint_pformat                   | 743 ms                                                                   | 752 ms: 1.01x slower                                                     |
| deepcopy_reduce                  | 1.27 us                                                                  | 1.29 us: 1.01x slower                                                    |
| html5lib                         | 23.3 ms                                                                  | 23.6 ms: 1.01x slower                                                    |
| async_generators                 | 178 ms                                                                   | 181 ms: 1.02x slower                                                     |
| json                             | 1.96 ms                                                                  | 1.99 ms: 1.02x slower                                                    |
| genshi_text                      | 11.2 ms                                                                  | 11.5 ms: 1.02x slower                                                    |
| sympy_integrate                  | 8.07 ms                                                                  | 8.22 ms: 1.02x slower                                                    |
| scimark_monte_carlo              | 32.8 ms                                                                  | 33.4 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                                   | 165 ms: 1.02x slower                                                     |
| django_template                  | 16.6 ms                                                                  | 17.0 ms: 1.02x slower                                                    |
| shortest_path                    | 225 ms                                                                   | 231 ms: 1.02x slower                                                     |
| nbody                            | 52.8 ms                                                                  | 54.3 ms: 1.03x slower                                                    |
| tomli_loads                      | 949 ms                                                                   | 976 ms: 1.03x slower                                                     |
| sqlglot_v2_transpile             | 712 us                                                                   | 733 us: 1.03x slower                                                     |
| raytrace                         | 128 ms                                                                   | 132 ms: 1.03x slower                                                     |
| go                               | 61.7 ms                                                                  | 63.5 ms: 1.03x slower                                                    |
| logging_format                   | 2.78 us                                                                  | 2.87 us: 1.03x slower                                                    |
| logging_simple                   | 2.51 us                                                                  | 2.60 us: 1.04x slower                                                    |
| richards                         | 23.8 ms                                                                  | 24.8 ms: 1.04x slower                                                    |
| chaos                            | 28.4 ms                                                                  | 29.5 ms: 1.04x slower                                                    |
| many_optionals                   | 236 us                                                                   | 246 us: 1.04x slower                                                     |
| scimark_sparse_mat_mult          | 2.05 ms                                                                  | 2.13 ms: 1.04x slower                                                    |
| sqlglot_v2_parse                 | 583 us                                                                   | 608 us: 1.04x slower                                                     |
| generators                       | 18.2 ms                                                                  | 19.1 ms: 1.05x slower                                                    |
| comprehensions                   | 8.35 us                                                                  | 8.74 us: 1.05x slower                                                    |
| genshi_xml                       | 22.5 ms                                                                  | 23.6 ms: 1.05x slower                                                    |
| typing_runtime_protocols         | 69.6 us                                                                  | 72.9 us: 1.05x slower                                                    |
| regex_effbot                     | 1.43 ms                                                                  | 1.50 ms: 1.05x slower                                                    |
| telco                            | 3.23 ms                                                                  | 3.41 ms: 1.05x slower                                                    |
| sqlalchemy_imperative            | 5.48 ms                                                                  | 5.77 ms: 1.05x slower                                                    |
| logging_silent                   | 46.5 ns                                                                  | 49.2 ns: 1.06x slower                                                    |
| sympy_str                        | 106 ms                                                                   | 112 ms: 1.06x slower                                                     |
| 2to3                             | 115 ms                                                                   | 122 ms: 1.06x slower                                                     |
| connected_components             | 206 ms                                                                   | 219 ms: 1.06x slower                                                     |
| json_loads                       | 11.3 us                                                                  | 12.0 us: 1.06x slower                                                    |
| richards_super                   | 26.6 ms                                                                  | 28.3 ms: 1.06x slower                                                    |
| dulwich_log                      | 17.7 ms                                                                  | 19.0 ms: 1.07x slower                                                    |
| regex_compile                    | 50.3 ms                                                                  | 53.8 ms: 1.07x slower                                                    |
| sympy_sum                        | 57.8 ms                                                                  | 62.3 ms: 1.08x slower                                                    |
| deepcopy_memo                    | 13.4 us                                                                  | 14.5 us: 1.08x slower                                                    |
| sympy_expand                     | 177 ms                                                                   | 191 ms: 1.08x slower                                                     |
| regex_dna                        | 92.5 ms                                                                  | 101 ms: 1.10x slower                                                     |
| python_startup                   | 8.70 ms                                                                  | 9.53 ms: 1.10x slower                                                    |
| sqlalchemy_declarative           | 46.2 ms                                                                  | 50.8 ms: 1.10x slower                                                    |
| deepcopy                         | 114 us                                                                   | 125 us: 1.10x slower                                                     |
| mako                             | 5.06 ms                                                                  | 5.58 ms: 1.10x slower                                                    |
| async_tree_eager                 | 45.7 ms                                                                  | 51.2 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 37.5 ms                                                                  | 42.1 ms: 1.12x slower                                                    |
| meteor_contest                   | 50.3 ms                                                                  | 57.1 ms: 1.14x slower                                                    |
| python_startup_no_site           | 6.46 ms                                                                  | 7.58 ms: 1.17x slower                                                    |
| coverage                         | 32.9 ms                                                                  | 38.8 ms: 1.18x slower                                                    |
| bench_thread_pool                | 440 us                                                                   | 578 us: 1.31x slower                                                     |
| Geometric mean                   | (ref)                                                                    | 1.02x faster                                                             |

Benchmark hidden because not significant (5): mdp, subparsers, k_core, pylint, sphinx

- Geometric mean (including insignificant results): 1.030x faster

# HPT report

- Reliability score: 85.17% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x