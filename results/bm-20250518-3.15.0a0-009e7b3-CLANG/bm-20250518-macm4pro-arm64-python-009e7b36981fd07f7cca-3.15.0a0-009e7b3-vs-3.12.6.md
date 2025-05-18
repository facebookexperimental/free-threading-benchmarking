# Results vs. 3.12.6

- fork: python
- ref: 009e7b36981fd07f7cca
- machine: darwin-arm64
- commit hash: 009e7b3
- commit date: 2025-05-18
- overall geometric mean: 1.143x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.04x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                   |
| sphinx         | 434 ms                                                   | 407 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 239 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 243 ms: 1.97x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 242 ms: 1.90x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 102 ms: 1.69x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 107 ms: 1.66x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 144 ms: 1.55x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.85 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 170 ms: 1.22x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.3 ms: 1.16x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.7 ms: 2.67x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| nbody          | 54.2 ms                                                  | 49.6 ms: 1.09x faster                                                   |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.4 ms: 1.26x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.55 ms: 1.08x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.7 ms: 1.01x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 10.4 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.4 ms: 1.22x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 33.2 ms: 1.17x faster                                                   |
| tomli_loads          | 957 ms                                                   | 819 ms: 1.17x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 23.6 ms: 1.13x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.9 ms: 1.13x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 92.6 us: 1.11x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 135 us: 1.03x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.49 ms: 1.05x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.9 us: 1.09x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.54 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.12 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 19.5 ms: 1.12x faster                                                   |
| genshi_text     | 10.5 ms                                                  | 9.40 ms: 1.12x faster                                                   |
| mako            | 4.77 ms                                                  | 4.70 ms: 1.02x faster                                                   |
| django_template | 13.6 ms                                                  | 14.3 ms: 1.05x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.05x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.35 ms: 2.22x faster                                                   |
| mdp                              | 1.09 sec                                                 | 514 ms: 2.12x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 239 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 243 ms: 1.97x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 242 ms: 1.90x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 102 ms: 1.69x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 107 ms: 1.66x faster                                                    |
| deepcopy                         | 161 us                                                   | 99.4 us: 1.62x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 11.4 us: 1.61x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                    |
| generators                       | 21.9 ms                                                  | 14.0 ms: 1.57x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 144 ms: 1.55x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.85 ms: 1.38x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.36x faster                                                   |
| go                               | 70.0 ms                                                  | 51.5 ms: 1.36x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.28 us: 1.35x faster                                                   |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 43.4 ms: 1.26x faster                                                   |
| raytrace                         | 145 ms                                                   | 116 ms: 1.25x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.0 ms: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.4 ms: 1.22x faster                                                   |
| async_generators                 | 206 ms                                                   | 170 ms: 1.22x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.42 ms: 1.21x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.8 ms: 1.20x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.57 ms: 1.18x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 33.2 ms: 1.17x faster                                                   |
| k_core                           | 1.12 sec                                                 | 955 ms: 1.17x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 819 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                  |
| async_tree_eager                 | 45.6 ms                                                  | 39.3 ms: 1.16x faster                                                   |
| pylint                           | 128 ms                                                   | 111 ms: 1.15x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.9 ms: 1.15x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.3 us: 1.14x faster                                                   |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 23.6 ms: 1.13x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 59.9 ms: 1.13x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 45.5 ms: 1.13x faster                                                   |
| richards                         | 22.4 ms                                                  | 19.9 ms: 1.12x faster                                                   |
| thrift                           | 322 us                                                   | 286 us: 1.12x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.8 ms: 1.12x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 19.5 ms: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 22.8 ms: 1.12x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.40 ms: 1.12x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.9 ms: 1.11x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 92.6 us: 1.11x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 49.2 ms: 1.11x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.30 ms: 1.10x faster                                                   |
| sympy_str                        | 104 ms                                                   | 95.2 ms: 1.09x faster                                                   |
| nbody                            | 54.2 ms                                                  | 49.6 ms: 1.09x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 52.7 ms: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.55 ms: 1.08x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 618 ms: 1.08x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.39 us: 1.07x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 306 ms: 1.07x faster                                                    |
| sphinx                           | 434 ms                                                   | 407 ms: 1.06x faster                                                    |
| pycparser                        | 497 ms                                                   | 472 ms: 1.05x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 159 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                    |
| 2to3                             | 114 ms                                                   | 110 ms: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.5 ms: 1.03x faster                                                   |
| pickle_pure_python               | 139 us                                                   | 135 us: 1.03x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.02 ms: 1.03x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 945 ns: 1.02x faster                                                    |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.70 ms: 1.02x faster                                                   |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.01x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 98.7 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| connected_components             | 201 ms                                                   | 201 ms: 1.00x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 421 us: 1.00x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.1 ms: 1.01x slower                                                   |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.04x slower                                                   |
| django_template                  | 13.6 ms                                                  | 14.3 ms: 1.05x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.49 ms: 1.05x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.54 ms: 1.07x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.12 ms: 1.07x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 10.4 ms: 1.08x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.9 us: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.9 ms: 1.11x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 934 us: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                   |
| coverage                         | 26.9 ms                                                  | 31.6 ms: 1.18x slower                                                   |
| many_optionals                   | 195 us                                                   | 238 us: 1.22x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.7 ms: 2.67x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 196 ns: 3.85x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                            |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250518-3.15.0a0-009e7b3-CLANG/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.143x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.14x