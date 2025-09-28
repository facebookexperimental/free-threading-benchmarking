# Results vs. 3.13.0rc2

- fork: python
- ref: 48d0d0dd9733eae4935f
- machine: darwin-arm64
- commit hash: 48d0d0d
- commit date: 2025-09-26
- overall geometric mean: 1.026x faster
- HPT reliability: 98.75%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| html5lib       | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 251 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.27x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.9 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.0 ms: 3.01x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| float          | 31.4 ms                                                        | 31.0 ms: 1.01x faster                                                   |
| nbody          | 42.5 ms                                                        | 56.4 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                          | 1.08x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.68 ms: 1.10x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.1 ms: 1.01x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 48.3 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 813 ms: 1.23x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.7 ms: 1.08x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 92.9 us: 1.07x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 23.7 ms: 1.07x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.8 ms: 1.03x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.71 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.90 ms: 1.01x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.9 ms: 1.02x slower                                                   |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 251 ms: 2.08x faster                                                    |
| mdp                              | 1.06 sec                                                       | 544 ms: 1.94x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                    |
| k_core                           | 1.46 sec                                                       | 990 ms: 1.48x faster                                                    |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.28x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.27x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.5 ms: 1.27x faster                                                   |
| go                               | 72.6 ms                                                        | 57.4 ms: 1.26x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 813 ms: 1.23x faster                                                    |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.68 ms: 1.14x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.13 us: 1.14x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 288 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 585 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.68 ms: 1.10x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 914 us: 1.09x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.7 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                  |
| unpickle_pure_python             | 99.5 us                                                        | 92.9 us: 1.07x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.7 ms: 1.07x faster                                                   |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.05x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                   |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.9 ms: 1.03x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.4 ms: 1.03x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.0 ms: 1.03x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 60.8 ms: 1.03x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 927 ns: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 63.6 us: 1.02x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 122 ms: 1.02x faster                                                    |
| float                            | 31.4 ms                                                        | 31.0 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.5 ms: 1.01x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.90 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 43.9 ms: 1.00x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 95.1 ms: 1.01x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.3 ms: 1.01x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.71 ms: 1.01x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 2.87 ms: 1.01x slower                                                   |
| thrift                           | 309 us                                                         | 313 us: 1.01x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.4 ns: 1.02x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.02x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.9 ms: 1.02x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 423 us: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.32 us: 1.04x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                   |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.55 us: 1.04x slower                                                   |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 218 ms: 1.05x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.53 ms: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.5 ms: 1.06x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.2 ms: 1.06x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 39.7 ms: 1.06x slower                                                   |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.34 us: 1.08x slower                                                   |
| pycparser                        | 470 ms                                                         | 507 ms: 1.08x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 172 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.6 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.6 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 42.3 ms: 1.12x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.4 ms: 1.13x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.0 ms: 1.15x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.11 ms: 1.19x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.4 ms: 1.33x slower                                                   |
| many_optionals                   | 200 us                                                         | 330 us: 1.65x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.9 ms: 2.85x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.0 ms: 3.01x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (5): sphinx, mako, sympy_integrate, gc_traversal, docutils
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250926-3.15.0a0-48d0d0d-JIT/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.026x faster

# HPT report

- Reliability score: 98.75% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x