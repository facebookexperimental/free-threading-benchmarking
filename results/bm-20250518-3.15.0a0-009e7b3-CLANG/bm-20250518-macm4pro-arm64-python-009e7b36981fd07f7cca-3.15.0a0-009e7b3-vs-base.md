# Results vs. base

- fork: python
- ref: 009e7b36981fd07f7cca
- machine: darwin-arm64
- commit hash: 009e7b3
- commit date: 2025-05-18
- overall geometric mean: 1.041x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json | results/bm-20250518-3.15.0a0-009e7b3-CLANG/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 115 ms                                                                                                            | 110 ms: 1.05x faster                                                                                                    |
| html5lib       | 26.2 ms                                                                                                           | 22.4 ms: 1.17x faster                                                                                                   |
| sphinx         | 413 ms                                                                                                            | 407 ms: 1.01x faster                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.06x faster                                                                                                            |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json | results/bm-20250518-3.15.0a0-009e7b3-CLANG/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_eager                 | 42.2 ms                                                                                                           | 39.3 ms: 1.08x faster                                                                                                   |
| coroutines                       | 10.5 ms                                                                                                           | 9.85 ms: 1.07x faster                                                                                                   |
| async_tree_io                    | 255 ms                                                                                                            | 242 ms: 1.05x faster                                                                                                    |
| async_generators                 | 177 ms                                                                                                            | 170 ms: 1.04x faster                                                                                                    |
| async_tree_eager_io_tg           | 254 ms                                                                                                            | 245 ms: 1.04x faster                                                                                                    |
| async_tree_eager_io              | 247 ms                                                                                                            | 239 ms: 1.03x faster                                                                                                    |
| async_tree_none                  | 111 ms                                                                                                            | 107 ms: 1.03x faster                                                                                                    |
| async_tree_eager_memoization     | 111 ms                                                                                                            | 108 ms: 1.03x faster                                                                                                    |
| async_tree_io_tg                 | 250 ms                                                                                                            | 243 ms: 1.03x faster                                                                                                    |
| async_tree_none_tg               | 104 ms                                                                                                            | 102 ms: 1.02x faster                                                                                                    |
| async_tree_memoization           | 147 ms                                                                                                            | 144 ms: 1.02x faster                                                                                                    |
| async_tree_eager_tg              | 87.3 ms                                                                                                           | 85.7 ms: 1.02x faster                                                                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                                                                            | 221 ms: 1.02x faster                                                                                                    |
| async_tree_memoization_tg        | 148 ms                                                                                                            | 146 ms: 1.01x faster                                                                                                    |
| async_tree_eager_memoization_tg  | 131 ms                                                                                                            | 129 ms: 1.01x faster                                                                                                    |
| async_tree_cpu_io_mixed          | 267 ms                                                                                                            | 264 ms: 1.01x faster                                                                                                    |
| async_tree_eager_cpu_io_mixed_tg | 248 ms                                                                                                            | 245 ms: 1.01x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg       | 264 ms                                                                                                            | 262 ms: 1.01x faster                                                                                                    |
| Geometric mean                   | (ref)                                                                                                             | 1.02x faster                                                                                                            |

Benchmark hidden because not significant (3): asyncio_tcp_ssl, asyncio_websockets, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json | results/bm-20250518-3.15.0a0-009e7b3-CLANG/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 29.7 ms                                                                                                           | 28.5 ms: 1.04x faster                                                                                                   |
| Geometric mean | (ref)                                                                                                             | 1.01x faster                                                                                                            |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json | results/bm-20250518-3.15.0a0-009e7b3-CLANG/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 48.6 ms                                                                                                           | 43.4 ms: 1.12x faster                                                                                                   |
| regex_dna      | 102 ms                                                                                                            | 98.7 ms: 1.03x faster                                                                                                   |
| regex_v8       | 9.99 ms                                                                                                           | 10.4 ms: 1.04x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                             | 1.03x faster                                                                                                            |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json | results/bm-20250518-3.15.0a0-009e7b3-CLANG/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 960 ms                                                                                                            | 819 ms: 1.17x faster                                                                                                    |
| xml_etree_process    | 25.5 ms                                                                                                           | 23.6 ms: 1.08x faster                                                                                                   |
| xml_etree_generate   | 35.9 ms                                                                                                           | 33.2 ms: 1.08x faster                                                                                                   |
| unpickle_pure_python | 99.0 us                                                                                                           | 92.6 us: 1.07x faster                                                                                                   |
| pickle_pure_python   | 144 us                                                                                                            | 135 us: 1.07x faster                                                                                                    |
| xml_etree_parse      | 62.8 ms                                                                                                           | 59.9 ms: 1.05x faster                                                                                                   |
| xml_etree_iterparse  | 43.7 ms                                                                                                           | 42.4 ms: 1.03x faster                                                                                                   |
| json_dumps           | 4.61 ms                                                                                                           | 4.49 ms: 1.03x faster                                                                                                   |
| pickle_dict          | 12.9 us                                                                                                           | 12.8 us: 1.00x faster                                                                                                   |
| unpickle             | 6.22 us                                                                                                           | 6.25 us: 1.01x slower                                                                                                   |
| pickle_list          | 2.14 us                                                                                                           | 2.15 us: 1.01x slower                                                                                                   |
| json_loads           | 11.7 us                                                                                                           | 11.9 us: 1.02x slower                                                                                                   |
| unpickle_list        | 1.97 us                                                                                                           | 2.00 us: 1.02x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.04x faster                                                                                                            |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json | results/bm-20250518-3.15.0a0-009e7b3-CLANG/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 21.7 ms                                                                                                           | 19.5 ms: 1.11x faster                                                                                                   |
| django_template | 15.4 ms                                                                                                           | 14.3 ms: 1.08x faster                                                                                                   |
| genshi_text     | 9.94 ms                                                                                                           | 9.40 ms: 1.06x faster                                                                                                   |
| mako            | 4.80 ms                                                                                                           | 4.70 ms: 1.02x faster                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.07x faster                                                                                                            |

All benchmarks:
===============

| Benchmark                        | results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json | results/bm-20250518-3.15.0a0-009e7b3-CLANG/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| generators                       | 17.3 ms                                                                                                           | 14.0 ms: 1.24x faster                                                                                                   |
| tomli_loads                      | 960 ms                                                                                                            | 819 ms: 1.17x faster                                                                                                    |
| html5lib                         | 26.2 ms                                                                                                           | 22.4 ms: 1.17x faster                                                                                                   |
| regex_compile                    | 48.6 ms                                                                                                           | 43.4 ms: 1.12x faster                                                                                                   |
| deepcopy                         | 111 us                                                                                                            | 99.4 us: 1.12x faster                                                                                                   |
| genshi_xml                       | 21.7 ms                                                                                                           | 19.5 ms: 1.11x faster                                                                                                   |
| go                               | 57.0 ms                                                                                                           | 51.5 ms: 1.11x faster                                                                                                   |
| richards                         | 21.9 ms                                                                                                           | 19.9 ms: 1.10x faster                                                                                                   |
| deepcopy_memo                    | 12.4 us                                                                                                           | 11.4 us: 1.09x faster                                                                                                   |
| sqlglot_v2_parse                 | 550 us                                                                                                            | 503 us: 1.09x faster                                                                                                    |
| sqlglot_v2_transpile             | 671 us                                                                                                            | 618 us: 1.09x faster                                                                                                    |
| xml_etree_process                | 25.5 ms                                                                                                           | 23.6 ms: 1.08x faster                                                                                                   |
| richards_super                   | 24.6 ms                                                                                                           | 22.8 ms: 1.08x faster                                                                                                   |
| xml_etree_generate               | 35.9 ms                                                                                                           | 33.2 ms: 1.08x faster                                                                                                   |
| scimark_lu                       | 49.0 ms                                                                                                           | 45.5 ms: 1.08x faster                                                                                                   |
| deepcopy_reduce                  | 1.16 us                                                                                                           | 1.07 us: 1.08x faster                                                                                                   |
| hexiom                           | 2.77 ms                                                                                                           | 2.57 ms: 1.08x faster                                                                                                   |
| django_template                  | 15.4 ms                                                                                                           | 14.3 ms: 1.08x faster                                                                                                   |
| async_tree_eager                 | 42.2 ms                                                                                                           | 39.3 ms: 1.08x faster                                                                                                   |
| comprehensions                   | 7.79 us                                                                                                           | 7.28 us: 1.07x faster                                                                                                   |
| unpickle_pure_python             | 99.0 us                                                                                                           | 92.6 us: 1.07x faster                                                                                                   |
| coroutines                       | 10.5 ms                                                                                                           | 9.85 ms: 1.07x faster                                                                                                   |
| logging_format                   | 2.77 us                                                                                                           | 2.60 us: 1.07x faster                                                                                                   |
| logging_simple                   | 2.55 us                                                                                                           | 2.39 us: 1.07x faster                                                                                                   |
| pickle_pure_python               | 144 us                                                                                                            | 135 us: 1.07x faster                                                                                                    |
| sqlglot_v2_normalize             | 47.1 ms                                                                                                           | 44.2 ms: 1.07x faster                                                                                                   |
| sympy_sum                        | 56.1 ms                                                                                                           | 52.7 ms: 1.06x faster                                                                                                   |
| typing_runtime_protocols         | 66.2 us                                                                                                           | 62.3 us: 1.06x faster                                                                                                   |
| deltablue                        | 1.50 ms                                                                                                           | 1.42 ms: 1.06x faster                                                                                                   |
| thrift                           | 303 us                                                                                                            | 286 us: 1.06x faster                                                                                                    |
| genshi_text                      | 9.94 ms                                                                                                           | 9.40 ms: 1.06x faster                                                                                                   |
| sqlglot_v2_optimize              | 22.9 ms                                                                                                           | 21.7 ms: 1.06x faster                                                                                                   |
| meteor_contest                   | 50.8 ms                                                                                                           | 48.1 ms: 1.06x faster                                                                                                   |
| async_tree_io                    | 255 ms                                                                                                            | 242 ms: 1.05x faster                                                                                                    |
| dulwich_log                      | 17.9 ms                                                                                                           | 17.0 ms: 1.05x faster                                                                                                   |
| xml_etree_parse                  | 62.8 ms                                                                                                           | 59.9 ms: 1.05x faster                                                                                                   |
| 2to3                             | 115 ms                                                                                                            | 110 ms: 1.05x faster                                                                                                    |
| sympy_str                        | 99.5 ms                                                                                                           | 95.2 ms: 1.05x faster                                                                                                   |
| coverage                         | 33.0 ms                                                                                                           | 31.6 ms: 1.05x faster                                                                                                   |
| async_generators                 | 177 ms                                                                                                            | 170 ms: 1.04x faster                                                                                                    |
| pprint_pformat                   | 645 ms                                                                                                            | 618 ms: 1.04x faster                                                                                                    |
| many_optionals                   | 248 us                                                                                                            | 238 us: 1.04x faster                                                                                                    |
| pycparser                        | 492 ms                                                                                                            | 472 ms: 1.04x faster                                                                                                    |
| float                            | 29.7 ms                                                                                                           | 28.5 ms: 1.04x faster                                                                                                   |
| sympy_expand                     | 166 ms                                                                                                            | 159 ms: 1.04x faster                                                                                                    |
| subparsers                       | 9.74 ms                                                                                                           | 9.35 ms: 1.04x faster                                                                                                   |
| pprint_safe_repr                 | 318 ms                                                                                                            | 306 ms: 1.04x faster                                                                                                    |
| fannkuch                         | 179 ms                                                                                                            | 172 ms: 1.04x faster                                                                                                    |
| bench_thread_pool                | 436 us                                                                                                            | 421 us: 1.04x faster                                                                                                    |
| async_tree_eager_io_tg           | 254 ms                                                                                                            | 245 ms: 1.04x faster                                                                                                    |
| scimark_fft                      | 136 ms                                                                                                            | 131 ms: 1.04x faster                                                                                                    |
| pylint                           | 115 ms                                                                                                            | 111 ms: 1.03x faster                                                                                                    |
| pyflate                          | 197 ms                                                                                                            | 191 ms: 1.03x faster                                                                                                    |
| async_tree_eager_io              | 247 ms                                                                                                            | 239 ms: 1.03x faster                                                                                                    |
| scimark_sor                      | 52.4 ms                                                                                                           | 50.8 ms: 1.03x faster                                                                                                   |
| regex_dna                        | 102 ms                                                                                                            | 98.7 ms: 1.03x faster                                                                                                   |
| async_tree_none                  | 111 ms                                                                                                            | 107 ms: 1.03x faster                                                                                                    |
| xml_etree_iterparse              | 43.7 ms                                                                                                           | 42.4 ms: 1.03x faster                                                                                                   |
| async_tree_eager_memoization     | 111 ms                                                                                                            | 108 ms: 1.03x faster                                                                                                    |
| async_tree_io_tg                 | 250 ms                                                                                                            | 243 ms: 1.03x faster                                                                                                    |
| json_dumps                       | 4.61 ms                                                                                                           | 4.49 ms: 1.03x faster                                                                                                   |
| raytrace                         | 119 ms                                                                                                            | 116 ms: 1.03x faster                                                                                                    |
| scimark_monte_carlo              | 29.7 ms                                                                                                           | 28.9 ms: 1.03x faster                                                                                                   |
| async_tree_none_tg               | 104 ms                                                                                                            | 102 ms: 1.02x faster                                                                                                    |
| sympy_integrate                  | 7.47 ms                                                                                                           | 7.30 ms: 1.02x faster                                                                                                   |
| chaos                            | 26.4 ms                                                                                                           | 25.8 ms: 1.02x faster                                                                                                   |
| mako                             | 4.80 ms                                                                                                           | 4.70 ms: 1.02x faster                                                                                                   |
| async_tree_memoization           | 147 ms                                                                                                            | 144 ms: 1.02x faster                                                                                                    |
| mdp                              | 524 ms                                                                                                            | 514 ms: 1.02x faster                                                                                                    |
| async_tree_eager_tg              | 87.3 ms                                                                                                           | 85.7 ms: 1.02x faster                                                                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                                                                            | 221 ms: 1.02x faster                                                                                                    |
| pathlib                          | 11.2 ms                                                                                                           | 11.1 ms: 1.02x faster                                                                                                   |
| crypto_pyaes                     | 38.1 ms                                                                                                           | 37.5 ms: 1.02x faster                                                                                                   |
| telco                            | 3.06 ms                                                                                                           | 3.02 ms: 1.01x faster                                                                                                   |
| sphinx                           | 413 ms                                                                                                            | 407 ms: 1.01x faster                                                                                                    |
| async_tree_memoization_tg        | 148 ms                                                                                                            | 146 ms: 1.01x faster                                                                                                    |
| async_tree_eager_memoization_tg  | 131 ms                                                                                                            | 129 ms: 1.01x faster                                                                                                    |
| async_tree_cpu_io_mixed          | 267 ms                                                                                                            | 264 ms: 1.01x faster                                                                                                    |
| nqueens                          | 38.2 ms                                                                                                           | 37.9 ms: 1.01x faster                                                                                                   |
| async_tree_eager_cpu_io_mixed_tg | 248 ms                                                                                                            | 245 ms: 1.01x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg       | 264 ms                                                                                                            | 262 ms: 1.01x faster                                                                                                    |
| bpe_tokeniser                    | 1.94 sec                                                                                                          | 1.93 sec: 1.01x faster                                                                                                  |
| sqlite_synth                     | 950 ns                                                                                                            | 945 ns: 1.01x faster                                                                                                    |
| pickle_dict                      | 12.9 us                                                                                                           | 12.8 us: 1.00x faster                                                                                                   |
| dask                             | 521 ms                                                                                                            | 523 ms: 1.00x slower                                                                                                    |
| logging_silent                   | 195 ns                                                                                                            | 196 ns: 1.01x slower                                                                                                    |
| create_gc_cycles                 | 929 us                                                                                                            | 934 us: 1.01x slower                                                                                                    |
| unpickle                         | 6.22 us                                                                                                           | 6.25 us: 1.01x slower                                                                                                   |
| pickle_list                      | 2.14 us                                                                                                           | 2.15 us: 1.01x slower                                                                                                   |
| gc_traversal                     | 2.07 ms                                                                                                           | 2.08 ms: 1.01x slower                                                                                                   |
| shortest_path                    | 214 ms                                                                                                            | 216 ms: 1.01x slower                                                                                                    |
| connected_components             | 198 ms                                                                                                            | 201 ms: 1.01x slower                                                                                                    |
| scimark_sparse_mat_mult          | 1.99 ms                                                                                                           | 2.02 ms: 1.02x slower                                                                                                   |
| json_loads                       | 11.7 us                                                                                                           | 11.9 us: 1.02x slower                                                                                                   |
| unpickle_list                    | 1.97 us                                                                                                           | 2.00 us: 1.02x slower                                                                                                   |
| spectral_norm                    | 47.7 ms                                                                                                           | 49.2 ms: 1.03x slower                                                                                                   |
| regex_v8                         | 9.99 ms                                                                                                           | 10.4 ms: 1.04x slower                                                                                                   |
| unpack_sequence                  | 30.4 ns                                                                                                           | 33.9 ns: 1.12x slower                                                                                                   |
| Geometric mean                   | (ref)                                                                                                             | 1.04x faster                                                                                                            |

Benchmark hidden because not significant (13): asyncio_tcp_ssl, pidigits, bench_mp_pool, python_startup_no_site, python_startup, asyncio_websockets, docutils, nbody, pickle, regex_effbot, json, k_core, asyncio_tcp

- Geometric mean (including insignificant results): 1.041x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.01x