# Results vs. 3.12.6

- fork: python
- ref: 48d0d0dd9733eae4935f
- machine: darwin-arm64
- commit hash: 48d0d0d
- commit date: 2025-09-26
- overall geometric mean: 1.099x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                   |
| sphinx         | 434 ms                                                   | 405 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 253 ms: 1.90x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.2 ms: 1.08x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.4 ms: 1.21x faster                                                   |
| nbody          | 54.2 ms                                                  | 50.5 ms: 1.07x faster                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.4 ms: 1.04x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.78 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.8 ms: 1.21x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 61.3 ms: 1.11x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.87 ms: 1.10x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.2 ms: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 102 us: 1.01x faster                                                    |
| tomli_loads          | 957 ms                                                   | 948 ms: 1.01x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 150 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.9 ms: 1.01x slower                                                   |
| mako            | 4.77 ms                                                  | 5.06 ms: 1.06x slower                                                   |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 543 ms: 2.01x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 253 ms: 1.90x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                    |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.30x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.57 us: 1.30x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.5 ms: 1.26x faster                                                   |
| go                               | 70.0 ms                                                  | 57.0 ms: 1.23x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.7 ns: 1.22x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 44.6 ms: 1.22x faster                                                   |
| float                            | 37.9 ms                                                  | 31.4 ms: 1.21x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.8 ms: 1.21x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                    |
| raytrace                         | 145 ms                                                   | 121 ms: 1.19x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.4 ms: 1.18x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 52.1 ms: 1.17x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 17.8 ms: 1.17x faster                                                   |
| k_core                           | 1.12 sec                                                 | 959 ms: 1.17x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.50 ms: 1.15x faster                                                   |
| pylint                           | 128 ms                                                   | 112 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| typing_runtime_protocols         | 71.0 us                                                  | 63.1 us: 1.12x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.85 ms: 1.12x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 61.3 ms: 1.11x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 39.3 ms: 1.11x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.87 ms: 1.10x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.09x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.57 us: 1.09x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.36 ms: 1.09x faster                                                   |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.2 ms: 1.08x faster                                                   |
| nbody                            | 54.2 ms                                                  | 50.5 ms: 1.07x faster                                                   |
| chaos                            | 28.9 ms                                                  | 27.0 ms: 1.07x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.2 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 405 ms: 1.07x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.86 ms: 1.06x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.6 ms: 1.06x faster                                                   |
| sympy_str                        | 104 ms                                                   | 98.8 ms: 1.05x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.7 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 95.4 ms: 1.04x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.4 ms: 1.04x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.5 ms: 1.04x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.6 ms: 1.04x faster                                                   |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                   |
| thrift                           | 322 us                                                   | 315 us: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 950 ns: 1.02x faster                                                    |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 102 us: 1.01x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 948 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 220 ms: 1.00x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.9 ms: 1.01x slower                                                   |
| connected_components             | 201 ms                                                   | 202 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 423 us: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 672 ms: 1.01x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.03 ms: 1.01x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| regex_v8                         | 9.59 ms                                                  | 9.78 ms: 1.02x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 336 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.2 ms: 1.03x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 41.5 ms: 1.05x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.06 ms: 1.06x slower                                                   |
| fannkuch                         | 176 ms                                                   | 189 ms: 1.08x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 150 us: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.86 ms: 1.10x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 924 us: 1.11x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 319 us: 1.64x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (2): pycparser, pidigits
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250926-3.15.0a0-48d0d0d/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.099x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x