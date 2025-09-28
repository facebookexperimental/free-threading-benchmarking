# Results vs. 3.13.0rc2

- fork: python
- ref: 48d0d0dd9733eae4935f
- machine: darwin-arm64
- commit hash: 48d0d0d
- commit date: 2025-09-26
- overall geometric mean: 1.020x faster
- HPT reliability: 88.76%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.01x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 24.4 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.5 ms: 3.03x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 50.5 ms: 1.19x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.4 ms: 1.01x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.87 ms: 1.20x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.8 ms: 1.08x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 948 ms: 1.05x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.2 ms: 1.01x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.7 ms: 1.01x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 102 us: 1.02x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 150 us: 1.15x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.9 ms: 1.02x slower                                                   |
| mako            | 4.41 ms                                                        | 5.06 ms: 1.15x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                    |
| mdp                              | 1.06 sec                                                       | 543 ms: 1.95x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                    |
| k_core                           | 1.46 sec                                                       | 959 ms: 1.53x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                   |
| go                               | 72.6 ms                                                        | 57.0 ms: 1.27x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 52.1 ms: 1.23x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.87 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.8 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 924 us: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.86 ms: 1.07x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 948 ms: 1.05x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 63.1 us: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.36 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.6 ms: 1.02x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.5 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.03 ms: 1.00x faster                                                   |
| python_startup                   | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 2.86 ms: 1.00x slower                                                   |
| 2to3                             | 112 ms                                                         | 112 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.4 ms: 1.01x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.2 ms: 1.01x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.7 ms: 1.01x slower                                                   |
| thrift                           | 309 us                                                         | 315 us: 1.02x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.6 ms: 1.02x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 102 us: 1.02x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.9 ms: 1.02x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.7 ms: 1.03x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 41.7 ns: 1.03x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 423 us: 1.03x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 672 ms: 1.03x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.8 ms: 1.04x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.04x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.85 ms: 1.04x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 336 ms: 1.04x slower                                                    |
| pycparser                        | 470 ms                                                         | 493 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.57 us: 1.05x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.4 ms: 1.05x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 39.3 ms: 1.05x slower                                                   |
| fannkuch                         | 179 ms                                                         | 189 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.4 ms: 1.06x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 41.5 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.1 ms: 1.10x slower                                                   |
| chaos                            | 24.3 ms                                                        | 27.0 ms: 1.11x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.11x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.57 us: 1.11x slower                                                   |
| raytrace                         | 109 ms                                                         | 121 ms: 1.12x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 48.6 ms: 1.14x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.06 ms: 1.15x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 150 us: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| nbody                            | 42.5 ms                                                        | 50.5 ms: 1.19x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| many_optionals                   | 200 us                                                         | 319 us: 1.59x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.8 ms: 2.84x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.5 ms: 3.03x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (3): sphinx, float, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250926-3.15.0a0-48d0d0d/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.020x faster

# HPT report

- Reliability score: 88.76% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x