# Results vs. 3.13.0rc2

- fork: python
- ref: 48d0d0dd9733eae4935f
- machine: darwin-arm64
- commit hash: 48d0d0d
- commit date: 2025-09-26
- overall geometric mean: 1.015x faster
- HPT reliability: 58.52%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 981 ms: 1.07x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.59x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.5 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.00x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.9 ms: 1.13x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.0 ms: 2.69x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.6 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.2 ms: 1.32x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.37 ms: 1.14x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.1 ms: 1.01x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.8 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.3 ms: 1.23x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 3.91 ms: 1.19x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.5 ms: 1.07x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 955 ms: 1.05x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.11x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.50 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.90 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.9 ms: 1.12x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.6 ms: 1.16x slower                                                   |
| mako            | 4.41 ms                                                        | 5.70 ms: 1.29x slower                                                   |
| django_template | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.22x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 749 us: 2.72x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.59x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 472 us: 2.11x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| mdp                              | 1.06 sec                                                       | 597 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.5 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 993 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                    |
| deepcopy                         | 145 us                                                         | 115 us: 1.26x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.25x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.3 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.91 ms: 1.19x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.1 ms: 1.16x faster                                                   |
| go                               | 72.6 ms                                                        | 62.5 ms: 1.16x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.37 ms: 1.14x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 836 ns: 1.13x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                   |
| docutils                         | 1.05 sec                                                       | 981 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.07x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 58.5 ms: 1.07x faster                                                   |
| float                            | 31.4 ms                                                        | 29.6 ms: 1.06x faster                                                   |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 955 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.04x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.04x faster                                                   |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| pycparser                        | 470 ms                                                         | 462 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.05 ms: 1.00x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.00x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 95.1 ms: 1.01x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| dask                             | 525 ms                                                         | 530 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| fannkuch                         | 179 ms                                                         | 186 ms: 1.04x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.98 ms: 1.06x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| pylint                           | 106 ms                                                         | 112 ms: 1.07x slower                                                    |
| connected_components             | 208 ms                                                         | 222 ms: 1.07x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.6 ms: 1.07x slower                                                   |
| thrift                           | 309 us                                                         | 334 us: 1.08x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 134 ms: 1.08x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 350 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 710 ms: 1.09x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.0 ms: 1.09x slower                                                   |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.50 ms: 1.10x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 44.7 ns: 1.10x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.8 ms: 1.10x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 42.0 ms: 1.11x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.11x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.49 us: 1.12x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.9 ms: 1.12x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.12x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 48.9 ms: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.7 us: 1.14x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.79 us: 1.14x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.3 ms: 1.15x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.6 ms: 1.16x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.90 ms: 1.16x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 50.8 ms: 1.16x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 55.9 ms: 1.17x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 43.6 ms: 1.17x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.7 ms: 1.19x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.13 ms: 1.20x slower                                                   |
| raytrace                         | 109 ms                                                         | 132 ms: 1.21x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.4 ms: 1.21x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.42 us: 1.24x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.8 ms: 1.27x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 54.9 ms: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.70 ms: 1.29x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.6 ms: 1.30x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.2 ms: 1.32x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 557 us: 1.35x slower                                                    |
| many_optionals                   | 200 us                                                         | 337 us: 1.68x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.0 ms: 2.69x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 19.0 ms: 3.03x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250926-3.15.0a0-48d0d0d-NOGIL/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.015x faster

# HPT report

- Reliability score: 58.52% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x