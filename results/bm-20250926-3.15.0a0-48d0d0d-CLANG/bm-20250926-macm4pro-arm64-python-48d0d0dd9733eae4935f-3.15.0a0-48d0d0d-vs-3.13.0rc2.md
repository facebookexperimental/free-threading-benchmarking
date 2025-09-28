# Results vs. 3.13.0rc2

- fork: python
- ref: 48d0d0dd9733eae4935f
- machine: darwin-arm64
- commit hash: 48d0d0d
- commit date: 2025-09-26
- overall geometric mean: 1.065x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 108 ms: 1.03x faster                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 22.1 ms: 1.05x faster                                                   |
| sphinx         | 409 ms                                                         | 398 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 238 ms: 2.21x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 244 ms: 2.14x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 245 ms: 1.65x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.32x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.30x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                    |
| async_generators                 | 193 ms                                                         | 170 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 258 ms: 1.14x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.0 ms: 1.11x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.2 ms: 2.91x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 47.7 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.4 ms: 1.10x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 11.0 ms: 1.03x slower                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.74 ms: 1.08x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 103 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 783 ms: 1.28x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.69 ms: 1.26x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 32.7 ms: 1.10x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 91.7 us: 1.09x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 23.5 ms: 1.08x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.8 ms: 1.05x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 135 us: 1.04x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 64.8 ms: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.57 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.15 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 19.7 ms: 1.08x faster                                                   |
| genshi_text     | 9.97 ms                                                        | 9.23 ms: 1.08x faster                                                   |
| mako            | 4.41 ms                                                        | 4.67 ms: 1.06x slower                                                   |
| django_template | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.00x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 238 ms: 2.21x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 244 ms: 2.14x faster                                                    |
| mdp                              | 1.06 sec                                                       | 517 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 245 ms: 1.65x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                    |
| k_core                           | 1.46 sec                                                       | 949 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 96.0 us: 1.51x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.1 us: 1.49x faster                                                   |
| go                               | 72.6 ms                                                        | 50.5 ms: 1.44x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.32x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.30x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.01 us: 1.28x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 783 ms: 1.28x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.2 ms: 1.28x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.69 ms: 1.26x faster                                                   |
| pyflate                          | 222 ms                                                         | 186 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.0 ms: 1.17x faster                                                   |
| richards                         | 22.1 ms                                                        | 19.0 ms: 1.16x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 21.7 ms: 1.14x faster                                                   |
| async_generators                 | 193 ms                                                         | 170 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 258 ms: 1.14x faster                                                    |
| generators                       | 15.7 ms                                                        | 14.0 ms: 1.12x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.56 ms: 1.11x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                  |
| async_tree_eager                 | 43.2 ms                                                        | 39.0 ms: 1.11x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 43.4 ms: 1.10x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.79 ms: 1.10x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 32.7 ms: 1.10x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 911 us: 1.09x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.2 ms: 1.09x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 91.7 us: 1.09x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 19.7 ms: 1.08x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.5 ms: 1.08x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.23 ms: 1.08x faster                                                   |
| float                            | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| json                             | 1.94 ms                                                        | 1.82 ms: 1.07x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 60.8 us: 1.06x faster                                                   |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.8 ms: 1.05x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.16 ms: 1.05x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 307 ms: 1.05x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.1 ms: 1.05x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 38.8 ns: 1.05x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 620 ms: 1.05x faster                                                    |
| thrift                           | 309 us                                                         | 296 us: 1.05x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.14 us: 1.04x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.36 us: 1.04x faster                                                   |
| 2to3                             | 112 ms                                                         | 108 ms: 1.03x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| sphinx                           | 409 ms                                                         | 398 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 219 ms: 1.02x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.2 ms: 1.02x faster                                                   |
| bench_thread_pool                | 412 us                                                         | 403 us: 1.02x faster                                                    |
| connected_components             | 208 ms                                                         | 204 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| sympy_str                        | 95.5 ms                                                        | 93.9 ms: 1.02x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 933 ns: 1.02x faster                                                    |
| sympy_expand                     | 159 ms                                                         | 157 ms: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| python_startup                   | 8.63 ms                                                        | 8.57 ms: 1.01x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 123 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 37.6 ms: 1.01x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 6.88 us: 1.01x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 52.9 ms: 1.01x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 44.7 ms: 1.02x slower                                                   |
| regex_v8                         | 10.7 ms                                                        | 11.0 ms: 1.03x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.15 ms: 1.03x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 135 us: 1.04x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 64.8 ms: 1.04x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 44.8 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.7 ms: 1.06x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.67 ms: 1.06x slower                                                   |
| raytrace                         | 109 ms                                                         | 115 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.90 ms: 1.07x slower                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.74 ms: 1.08x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 103 ms: 1.08x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 41.3 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.2 ms: 1.11x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.7 ms: 1.12x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 309 us: 1.54x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.1 ms: 2.73x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.2 ms: 2.91x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (3): pycparser, pylint, deltablue
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250926-3.15.0a0-48d0d0d-CLANG/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.065x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.09x