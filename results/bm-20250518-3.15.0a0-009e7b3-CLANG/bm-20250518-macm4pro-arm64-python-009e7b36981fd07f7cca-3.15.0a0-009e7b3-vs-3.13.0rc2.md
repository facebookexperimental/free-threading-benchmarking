# Results vs. 3.13.0rc2

- fork: python
- ref: 009e7b36981fd07f7cca
- machine: darwin-arm64
- commit hash: 009e7b3
- commit date: 2025-05-18
- overall geometric mean: 1.061x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.02x faster                                                    |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| html5lib       | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 239 ms: 2.20x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 245 ms: 2.12x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 243 ms: 1.66x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 242 ms: 1.59x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 107 ms: 1.33x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.30x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 144 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| async_generators                 | 193 ms                                                         | 170 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.3 ms: 1.10x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.85 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.7 ms: 2.96x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                   |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 49.6 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.4 ms: 1.10x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.55 ms: 1.04x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 98.7 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 819 ms: 1.22x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.4 ms: 1.09x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 33.2 ms: 1.08x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 23.6 ms: 1.08x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 92.6 us: 1.07x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.49 ms: 1.04x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 135 us: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.9 us: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.54 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.12 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 19.5 ms: 1.10x faster                                                   |
| genshi_text     | 9.97 ms                                                        | 9.40 ms: 1.06x faster                                                   |
| mako            | 4.41 ms                                                        | 4.70 ms: 1.07x slower                                                   |
| django_template | 12.5 ms                                                        | 14.3 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 239 ms: 2.20x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 245 ms: 2.12x faster                                                    |
| mdp                              | 1.06 sec                                                       | 514 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 243 ms: 1.66x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 242 ms: 1.59x faster                                                    |
| k_core                           | 1.46 sec                                                       | 955 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 99.4 us: 1.46x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.45x faster                                                   |
| go                               | 72.6 ms                                                        | 51.5 ms: 1.41x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 107 ms: 1.33x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.30x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 144 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.8 ms: 1.26x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 819 ms: 1.22x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.20x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 17.0 ms: 1.17x faster                                                   |
| pyflate                          | 222 ms                                                         | 191 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| async_generators                 | 193 ms                                                         | 170 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                    |
| generators                       | 15.7 ms                                                        | 14.0 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| richards                         | 22.1 ms                                                        | 19.9 ms: 1.11x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.57 ms: 1.11x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 43.4 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                  |
| float                            | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 39.3 ms: 1.10x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 19.5 ms: 1.10x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.85 ms: 1.09x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.4 ms: 1.09x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 22.8 ms: 1.08x faster                                                   |
| thrift                           | 309 us                                                         | 286 us: 1.08x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 33.2 ms: 1.08x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.6 ms: 1.08x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 92.6 us: 1.07x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 934 us: 1.06x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.40 ms: 1.06x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 306 ms: 1.05x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 618 ms: 1.05x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.55 ms: 1.04x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                   |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.3 us: 1.04x faster                                                   |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.49 ms: 1.04x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                   |
| connected_components             | 208 ms                                                         | 201 ms: 1.03x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.9 ms: 1.03x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.30 ms: 1.03x faster                                                   |
| deltablue                        | 1.45 ms                                                        | 1.42 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| 2to3                             | 112 ms                                                         | 110 ms: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.54 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| sympy_str                        | 95.5 ms                                                        | 95.2 ms: 1.00x faster                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.1 ms: 1.00x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| sympy_sum                        | 52.3 ms                                                        | 52.7 ms: 1.01x slower                                                   |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                   |
| coverage                         | 31.2 ms                                                        | 31.6 ms: 1.01x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 37.9 ms: 1.02x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 421 us: 1.02x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.12 ms: 1.03x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 135 us: 1.04x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 98.7 ms: 1.04x slower                                                   |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 45.5 ms: 1.06x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.8 ms: 1.06x slower                                                   |
| raytrace                         | 109 ms                                                         | 116 ms: 1.06x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.70 ms: 1.07x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.28 us: 1.07x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.39 us: 1.07x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.9 us: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.12x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 49.2 ms: 1.12x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.02 ms: 1.14x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.3 ms: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.9 ms: 1.16x slower                                                   |
| nbody                            | 42.5 ms                                                        | 49.6 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| many_optionals                   | 200 us                                                         | 238 us: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.35 ms: 1.49x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.7 ms: 2.96x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 196 ns: 4.83x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (4): sphinx, sqlite_synth, sympy_expand, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250518-3.15.0a0-009e7b3-CLANG/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.061x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.09x