# Results vs. 3.12.6

- fork: python
- ref: 48d0d0dd9733eae4935f
- machine: darwin-arm64
- commit hash: 48d0d0d
- commit date: 2025-09-26
- overall geometric mean: 1.094x faster
- HPT reliability: 98.78%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 981 ms: 1.04x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.5 ms: 1.99x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.9 ms: 1.07x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.0 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.6 ms: 1.28x faster                                                   |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| nbody          | 54.2 ms                                                  | 56.2 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.15x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.1 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.8 ms: 1.03x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.37 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.3 ms: 1.38x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.5 ms: 1.16x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.91 ms: 1.09x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.07x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 151 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.50 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.90 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.20x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.9 ms: 1.10x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.6 ms: 1.10x slower                                                   |
| mako            | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                   |
| django_template | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 749 us: 2.68x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.5 ms: 1.99x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.87x faster                                                    |
| mdp                              | 1.09 sec                                                 | 597 ms: 1.83x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 472 us: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| deepcopy                         | 161 us                                                   | 115 us: 1.40x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.2 us: 1.39x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.3 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                    |
| float                            | 37.9 ms                                                  | 29.6 ms: 1.28x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.20x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.4 ms: 1.19x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.7 ms: 1.17x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.42 us: 1.17x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 58.5 ms: 1.16x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 836 ns: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.15x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.15x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.7 ns: 1.14x faster                                                   |
| pylint                           | 128 ms                                                   | 112 ms: 1.14x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 993 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| go                               | 70.0 ms                                                  | 62.5 ms: 1.12x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.1 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 19.0 ms: 1.09x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.91 ms: 1.09x faster                                                   |
| pycparser                        | 497 ms                                                   | 462 ms: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.8 ms: 1.07x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 134 ms: 1.06x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 95.1 ms: 1.05x faster                                                   |
| docutils                         | 1.02 sec                                                 | 981 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.8 ms: 1.03x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.49 us: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.37 ms: 1.02x faster                                                   |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.98 ms: 1.01x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.79 us: 1.00x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 43.6 ms: 1.00x slower                                                   |
| dask                             | 528 ms                                                   | 530 ms: 1.00x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.4 ms: 1.02x slower                                                   |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.13 ms: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 334 us: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.2 ms: 1.04x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.7 us: 1.04x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.3 ms: 1.05x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.8 ms: 1.05x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.6 ms: 1.05x slower                                                   |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                    |
| fannkuch                         | 176 ms                                                   | 186 ms: 1.06x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 42.0 ms: 1.06x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.0 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 350 ms: 1.07x slower                                                    |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.07x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 710 ms: 1.07x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 54.9 ms: 1.07x slower                                                   |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.9 ms: 1.07x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.07x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 151 us: 1.08x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.9 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.8 ms: 1.10x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.6 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 222 ms: 1.10x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.05 ms: 1.17x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 55.9 ms: 1.17x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.50 ms: 1.18x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.90 ms: 1.21x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 557 us: 1.33x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.6 ms: 1.51x slower                                                   |
| many_optionals                   | 195 us                                                   | 337 us: 1.73x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.0 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (1): tomli_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250926-3.15.0a0-48d0d0d-NOGIL/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.094x faster

# HPT report

- Reliability score: 98.78% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x